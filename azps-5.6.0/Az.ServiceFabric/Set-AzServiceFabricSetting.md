---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976331"
---
# <span data-ttu-id="1b2c0-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1b2c0-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="1b2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2c0-103">클러스터에 하나 또는 여러 Service Fabric 설정을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="1b2c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b2c0-104">SYNTAX</span></span>

### <span data-ttu-id="1b2c0-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="1b2c0-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b2c0-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="1b2c0-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2c0-107">설명</span><span class="sxs-lookup"><span data-stu-id="1b2c0-107">DESCRIPTION</span></span>
<span data-ttu-id="1b2c0-108">**Set-AzServiceFabricSetting을** 사용하여 클러스터에서 Service Fabric 설정을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="1b2c0-109">예제</span><span class="sxs-lookup"><span data-stu-id="1b2c0-109">EXAMPLES</span></span>

### <span data-ttu-id="1b2c0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b2c0-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="1b2c0-111">이 명령은 'NamingService' 섹션에서 'MaxFileOperationTimeout'을 '5000'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="1b2c0-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1b2c0-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="1b2c0-113">이 명령은 SettingsSectionDescription 매개 변수를 사용하여 여러 패브릭 설정을 설정하는 업그레이드를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="1b2c0-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b2c0-114">PARAMETERS</span></span>

### <span data-ttu-id="1b2c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2c0-115">-DefaultProfile</span></span>
<span data-ttu-id="1b2c0-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1b2c0-117">-Name</span></span>
<span data-ttu-id="1b2c0-118">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="1b2c0-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-119">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b2c0-119">-Parameter</span></span>
<span data-ttu-id="1b2c0-120">패브릭 설정의 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="1b2c0-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b2c0-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-123">-Section</span><span class="sxs-lookup"><span data-stu-id="1b2c0-123">-Section</span></span>
<span data-ttu-id="1b2c0-124">패브릭 설정의 섹션 이름</span><span class="sxs-lookup"><span data-stu-id="1b2c0-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="1b2c0-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="1b2c0-126">패브릭 설정 배열</span><span class="sxs-lookup"><span data-stu-id="1b2c0-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-127">-Value</span><span class="sxs-lookup"><span data-stu-id="1b2c0-127">-Value</span></span>
<span data-ttu-id="1b2c0-128">패브릭 설정의 매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="1b2c0-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1b2c0-129">-Confirm</span></span>
<span data-ttu-id="1b2c0-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2c0-131">-WhatIf</span></span>
<span data-ttu-id="1b2c0-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2c0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2c0-134">CommonParameters</span></span>
<span data-ttu-id="1b2c0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2c0-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b2c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2c0-137">입력</span><span class="sxs-lookup"><span data-stu-id="1b2c0-137">INPUTS</span></span>

### <span data-ttu-id="1b2c0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1b2c0-138">System.String</span></span>

### <span data-ttu-id="1b2c0-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="1b2c0-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="1b2c0-140">출력</span><span class="sxs-lookup"><span data-stu-id="1b2c0-140">OUTPUTS</span></span>

### <span data-ttu-id="1b2c0-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="1b2c0-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1b2c0-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b2c0-142">NOTES</span></span>

## <span data-ttu-id="1b2c0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b2c0-143">RELATED LINKS</span></span>
