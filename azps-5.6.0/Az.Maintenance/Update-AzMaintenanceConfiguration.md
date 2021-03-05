---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985936"
---
# <span data-ttu-id="9295b-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9295b-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="9295b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9295b-102">SYNOPSIS</span></span>
<span data-ttu-id="9295b-103">패치 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="9295b-103">Patch configuration record</span></span>

## <span data-ttu-id="9295b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9295b-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9295b-105">설명</span><span class="sxs-lookup"><span data-stu-id="9295b-105">DESCRIPTION</span></span>
<span data-ttu-id="9295b-106">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="9295b-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="9295b-107">예제</span><span class="sxs-lookup"><span data-stu-id="9295b-107">EXAMPLES</span></span>

### <span data-ttu-id="9295b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9295b-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="9295b-109">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="9295b-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="9295b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9295b-110">PARAMETERS</span></span>

### <span data-ttu-id="9295b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9295b-111">-AsJob</span></span>
<span data-ttu-id="9295b-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9295b-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9295b-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="9295b-113">-Configuration</span></span>
<span data-ttu-id="9295b-114">업데이트할 유지 관리 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9295b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9295b-115">-DefaultProfile</span></span>
<span data-ttu-id="9295b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9295b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9295b-117">-Name</span></span>
<span data-ttu-id="9295b-118">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9295b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9295b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9295b-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="9295b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="9295b-121">-Confirm</span></span>
<span data-ttu-id="9295b-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9295b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9295b-123">-WhatIf</span></span>
<span data-ttu-id="9295b-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9295b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9295b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9295b-126">CommonParameters</span></span>
<span data-ttu-id="9295b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9295b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9295b-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9295b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9295b-129">입력</span><span class="sxs-lookup"><span data-stu-id="9295b-129">INPUTS</span></span>

### <span data-ttu-id="9295b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9295b-130">System.String</span></span>

### <span data-ttu-id="9295b-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9295b-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="9295b-132">출력</span><span class="sxs-lookup"><span data-stu-id="9295b-132">OUTPUTS</span></span>

### <span data-ttu-id="9295b-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9295b-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="9295b-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9295b-134">NOTES</span></span>

## <span data-ttu-id="9295b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9295b-135">RELATED LINKS</span></span>
