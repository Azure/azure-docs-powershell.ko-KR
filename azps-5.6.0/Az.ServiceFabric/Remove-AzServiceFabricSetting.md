---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 2df7c5f6af50bf581963f08e0544eb453f4b27df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005403"
---
# <span data-ttu-id="a9226-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a9226-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="a9226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9226-102">SYNOPSIS</span></span>
<span data-ttu-id="a9226-103">클러스터에서 하나 또는 여러 Service Fabric 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="a9226-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9226-104">SYNTAX</span></span>

### <span data-ttu-id="a9226-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="a9226-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9226-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="a9226-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9226-107">설명</span><span class="sxs-lookup"><span data-stu-id="a9226-107">DESCRIPTION</span></span>
<span data-ttu-id="a9226-108">**Remove-AzServiceFabricSetting을** 사용하여 클러스터에서 Service Fabric 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="a9226-109">예제</span><span class="sxs-lookup"><span data-stu-id="a9226-109">EXAMPLES</span></span>

### <span data-ttu-id="a9226-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9226-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="a9226-111">이 명령은 'EseStore' 섹션에서 'MaxCursors' 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="a9226-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9226-112">PARAMETERS</span></span>

### <span data-ttu-id="a9226-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9226-113">-DefaultProfile</span></span>
<span data-ttu-id="a9226-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9226-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a9226-115">-Name</span></span>
<span data-ttu-id="a9226-116">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="a9226-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a9226-117">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9226-117">-Parameter</span></span>
<span data-ttu-id="a9226-118">패브릭 설정의 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="a9226-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="a9226-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9226-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9226-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a9226-121">-Section</span><span class="sxs-lookup"><span data-stu-id="a9226-121">-Section</span></span>
<span data-ttu-id="a9226-122">패브릭 설정의 섹션 이름</span><span class="sxs-lookup"><span data-stu-id="a9226-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="a9226-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="a9226-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="a9226-124">패브릭 설정 배열</span><span class="sxs-lookup"><span data-stu-id="a9226-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="a9226-125">-확인</span><span class="sxs-lookup"><span data-stu-id="a9226-125">-Confirm</span></span>
<span data-ttu-id="a9226-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9226-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9226-127">-WhatIf</span></span>
<span data-ttu-id="a9226-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9226-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9226-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9226-130">CommonParameters</span></span>
<span data-ttu-id="a9226-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9226-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9226-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9226-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9226-133">입력</span><span class="sxs-lookup"><span data-stu-id="a9226-133">INPUTS</span></span>

### <span data-ttu-id="a9226-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a9226-134">System.String</span></span>

### <span data-ttu-id="a9226-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="a9226-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="a9226-136">출력</span><span class="sxs-lookup"><span data-stu-id="a9226-136">OUTPUTS</span></span>

### <span data-ttu-id="a9226-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a9226-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a9226-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9226-138">NOTES</span></span>

## <span data-ttu-id="a9226-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9226-139">RELATED LINKS</span></span>
