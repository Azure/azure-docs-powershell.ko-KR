---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191137"
---
# <span data-ttu-id="ae665-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ae665-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="ae665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae665-102">SYNOPSIS</span></span>
<span data-ttu-id="ae665-103">하나 또는 여러 Service Fabric 설정을 클러스터에 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="ae665-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae665-104">SYNTAX</span></span>

### <span data-ttu-id="ae665-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="ae665-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae665-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="ae665-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae665-107">설명</span><span class="sxs-lookup"><span data-stu-id="ae665-107">DESCRIPTION</span></span>
<span data-ttu-id="ae665-108">**Set-AzServiceFabricSetting을** 사용하여 클러스터에서 Service Fabric 설정을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="ae665-109">예제</span><span class="sxs-lookup"><span data-stu-id="ae665-109">EXAMPLES</span></span>

### <span data-ttu-id="ae665-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae665-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="ae665-111">이 명령은 'NamingService' 섹션에서 'MaxFileOperationTimeout'을 '5000' 값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="ae665-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ae665-112">Example 2</span></span>
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

<span data-ttu-id="ae665-113">이 명령은 SettingsSectionDescription 매개 변수를 사용하여 여러 패브릭 설정을 설정하는 업그레이드를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="ae665-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae665-114">PARAMETERS</span></span>

### <span data-ttu-id="ae665-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae665-115">-DefaultProfile</span></span>
<span data-ttu-id="ae665-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae665-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ae665-117">-Name</span></span>
<span data-ttu-id="ae665-118">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="ae665-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ae665-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ae665-119">-Parameter</span></span>
<span data-ttu-id="ae665-120">패브릭 설정의 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="ae665-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="ae665-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae665-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae665-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ae665-123">-Section</span><span class="sxs-lookup"><span data-stu-id="ae665-123">-Section</span></span>
<span data-ttu-id="ae665-124">패브릭 설정의 섹션 이름</span><span class="sxs-lookup"><span data-stu-id="ae665-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="ae665-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="ae665-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="ae665-126">패브릭 설정의 배열</span><span class="sxs-lookup"><span data-stu-id="ae665-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="ae665-127">-Value</span><span class="sxs-lookup"><span data-stu-id="ae665-127">-Value</span></span>
<span data-ttu-id="ae665-128">패브릭 설정의 매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="ae665-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="ae665-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae665-129">-Confirm</span></span>
<span data-ttu-id="ae665-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae665-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae665-131">-WhatIf</span></span>
<span data-ttu-id="ae665-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ae665-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae665-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae665-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae665-134">CommonParameters</span></span>
<span data-ttu-id="ae665-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae665-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae665-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae665-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae665-137">입력</span><span class="sxs-lookup"><span data-stu-id="ae665-137">INPUTS</span></span>

### <span data-ttu-id="ae665-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ae665-138">System.String</span></span>

### <span data-ttu-id="ae665-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="ae665-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="ae665-140">출력</span><span class="sxs-lookup"><span data-stu-id="ae665-140">OUTPUTS</span></span>

### <span data-ttu-id="ae665-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="ae665-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ae665-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae665-142">NOTES</span></span>

## <span data-ttu-id="ae665-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae665-143">RELATED LINKS</span></span>
