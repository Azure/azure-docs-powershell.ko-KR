---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358275"
---
# <span data-ttu-id="a9a42-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9a42-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="a9a42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9a42-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a42-103">패치 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="a9a42-103">Patch configuration record</span></span>

## <span data-ttu-id="a9a42-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9a42-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a42-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9a42-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a42-106">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="a9a42-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="a9a42-107">예제</span><span class="sxs-lookup"><span data-stu-id="a9a42-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a42-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9a42-108">Example 1</span></span>
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

<span data-ttu-id="a9a42-109">패치 유지 관리 구성 레코드</span><span class="sxs-lookup"><span data-stu-id="a9a42-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="a9a42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9a42-110">PARAMETERS</span></span>

### <span data-ttu-id="a9a42-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9a42-111">-AsJob</span></span>
<span data-ttu-id="a9a42-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a9a42-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9a42-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="a9a42-113">-Configuration</span></span>
<span data-ttu-id="a9a42-114">업데이트할 유지 관리 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="a9a42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a42-115">-DefaultProfile</span></span>
<span data-ttu-id="a9a42-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9a42-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9a42-117">-Name</span></span>
<span data-ttu-id="a9a42-118">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="a9a42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a42-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9a42-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="a9a42-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9a42-121">-Confirm</span></span>
<span data-ttu-id="a9a42-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a42-123">-WhatIf</span></span>
<span data-ttu-id="a9a42-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a9a42-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a42-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a42-126">CommonParameters</span></span>
<span data-ttu-id="a9a42-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9a42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a42-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9a42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a42-129">입력</span><span class="sxs-lookup"><span data-stu-id="a9a42-129">INPUTS</span></span>

### <span data-ttu-id="a9a42-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a42-130">System.String</span></span>

### <span data-ttu-id="a9a42-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9a42-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a9a42-132">출력</span><span class="sxs-lookup"><span data-stu-id="a9a42-132">OUTPUTS</span></span>

### <span data-ttu-id="a9a42-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9a42-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a9a42-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9a42-134">NOTES</span></span>

## <span data-ttu-id="a9a42-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9a42-135">RELATED LINKS</span></span>
