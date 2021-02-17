---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192265"
---
# <span data-ttu-id="773ab-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="773ab-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="773ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="773ab-102">SYNOPSIS</span></span>
<span data-ttu-id="773ab-103">패치 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="773ab-103">Patch configuration record</span></span>

## <span data-ttu-id="773ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="773ab-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="773ab-105">설명</span><span class="sxs-lookup"><span data-stu-id="773ab-105">DESCRIPTION</span></span>
<span data-ttu-id="773ab-106">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="773ab-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="773ab-107">예제</span><span class="sxs-lookup"><span data-stu-id="773ab-107">EXAMPLES</span></span>

### <span data-ttu-id="773ab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="773ab-108">Example 1</span></span>
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

<span data-ttu-id="773ab-109">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="773ab-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="773ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="773ab-110">PARAMETERS</span></span>

### <span data-ttu-id="773ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="773ab-111">-AsJob</span></span>
<span data-ttu-id="773ab-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="773ab-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="773ab-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="773ab-113">-Configuration</span></span>
<span data-ttu-id="773ab-114">업데이트할 유지 관리 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="773ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773ab-115">-DefaultProfile</span></span>
<span data-ttu-id="773ab-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773ab-117">-Name</span><span class="sxs-lookup"><span data-stu-id="773ab-117">-Name</span></span>
<span data-ttu-id="773ab-118">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="773ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="773ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="773ab-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="773ab-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="773ab-121">-Confirm</span></span>
<span data-ttu-id="773ab-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="773ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="773ab-123">-WhatIf</span></span>
<span data-ttu-id="773ab-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="773ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="773ab-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="773ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773ab-126">CommonParameters</span></span>
<span data-ttu-id="773ab-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="773ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773ab-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="773ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773ab-129">입력</span><span class="sxs-lookup"><span data-stu-id="773ab-129">INPUTS</span></span>

### <span data-ttu-id="773ab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="773ab-130">System.String</span></span>

### <span data-ttu-id="773ab-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="773ab-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="773ab-132">출력</span><span class="sxs-lookup"><span data-stu-id="773ab-132">OUTPUTS</span></span>

### <span data-ttu-id="773ab-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="773ab-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="773ab-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="773ab-134">NOTES</span></span>

## <span data-ttu-id="773ab-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="773ab-135">RELATED LINKS</span></span>
