---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044220"
---
# <span data-ttu-id="7c25e-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c25e-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="7c25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c25e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c25e-103">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c25e-103">Create or Update configuration record</span></span>

## <span data-ttu-id="7c25e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c25e-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c25e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c25e-105">DESCRIPTION</span></span>
<span data-ttu-id="7c25e-106">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c25e-106">Create or Update configuration record</span></span>

## <span data-ttu-id="7c25e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c25e-107">EXAMPLES</span></span>

### <span data-ttu-id="7c25e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c25e-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="7c25e-109">범위 호스트를 사용 하 여 유지 관리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="7c25e-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="7c25e-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c25e-110">PARAMETERS</span></span>

### <span data-ttu-id="7c25e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c25e-111">-AsJob</span></span>
<span data-ttu-id="7c25e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c25e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c25e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c25e-113">-DefaultProfile</span></span>
<span data-ttu-id="7c25e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c25e-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="7c25e-115">-ExtensionProperty</span></span>
<span data-ttu-id="7c25e-116">Resource 당 확장 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-117">-위치</span><span class="sxs-lookup"><span data-stu-id="7c25e-117">-Location</span></span>
<span data-ttu-id="7c25e-118">유지 관리 구성 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-118">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="7c25e-119">-MaintenanceScope</span></span>
<span data-ttu-id="7c25e-120">유지 관리 범위</span><span class="sxs-lookup"><span data-stu-id="7c25e-120">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7c25e-121">-Name</span></span>
<span data-ttu-id="7c25e-122">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="7c25e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c25e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c25e-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="7c25e-125">태그</span><span class="sxs-lookup"><span data-stu-id="7c25e-125">-Tag</span></span>
<span data-ttu-id="7c25e-126">ARM 태그.</span><span class="sxs-lookup"><span data-stu-id="7c25e-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c25e-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7c25e-127">-Confirm</span></span>
<span data-ttu-id="7c25e-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c25e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c25e-129">-WhatIf</span></span>
<span data-ttu-id="7c25e-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c25e-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c25e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c25e-132">CommonParameters</span></span>
<span data-ttu-id="7c25e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c25e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c25e-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c25e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c25e-135">입력</span><span class="sxs-lookup"><span data-stu-id="7c25e-135">INPUTS</span></span>

### <span data-ttu-id="7c25e-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c25e-136">System.String</span></span>

## <span data-ttu-id="7c25e-137">출력</span><span class="sxs-lookup"><span data-stu-id="7c25e-137">OUTPUTS</span></span>

### <span data-ttu-id="7c25e-138">PSMaintenanceConfiguration/. m m</span><span class="sxs-lookup"><span data-stu-id="7c25e-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7c25e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7c25e-139">NOTES</span></span>

## <span data-ttu-id="7c25e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c25e-140">RELATED LINKS</span></span>
