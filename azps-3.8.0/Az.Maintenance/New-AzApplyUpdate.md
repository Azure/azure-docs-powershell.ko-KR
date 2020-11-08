---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044227"
---
# <span data-ttu-id="53345-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="53345-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="53345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53345-102">SYNOPSIS</span></span>
<span data-ttu-id="53345-103">유지 관리 업데이트를 리소스에 적용</span><span class="sxs-lookup"><span data-stu-id="53345-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="53345-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53345-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53345-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53345-105">DESCRIPTION</span></span>
<span data-ttu-id="53345-106">유지 관리 업데이트를 리소스에 적용</span><span class="sxs-lookup"><span data-stu-id="53345-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="53345-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53345-107">EXAMPLES</span></span>

### <span data-ttu-id="53345-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="53345-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="53345-109">유지 관리 업데이트를 리소스에 적용</span><span class="sxs-lookup"><span data-stu-id="53345-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="53345-110">변수</span><span class="sxs-lookup"><span data-stu-id="53345-110">PARAMETERS</span></span>

### <span data-ttu-id="53345-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53345-111">-AsJob</span></span>
<span data-ttu-id="53345-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53345-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53345-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53345-113">-DefaultProfile</span></span>
<span data-ttu-id="53345-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53345-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="53345-115">-ProviderName</span></span>
<span data-ttu-id="53345-116">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="53345-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53345-117">-ResourceGroupName</span></span>
<span data-ttu-id="53345-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="53345-119">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="53345-119">-ResourceName</span></span>
<span data-ttu-id="53345-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53345-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="53345-121">-ResourceParentName</span></span>
<span data-ttu-id="53345-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53345-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="53345-123">-ResourceParentType</span></span>
<span data-ttu-id="53345-124">부모 리소스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53345-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="53345-125">-ResourceType</span></span>
<span data-ttu-id="53345-126">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="53345-126">The resource type.</span></span>

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

### <span data-ttu-id="53345-127">-확인</span><span class="sxs-lookup"><span data-stu-id="53345-127">-Confirm</span></span>
<span data-ttu-id="53345-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53345-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53345-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53345-129">-WhatIf</span></span>
<span data-ttu-id="53345-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53345-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53345-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53345-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53345-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53345-132">CommonParameters</span></span>
<span data-ttu-id="53345-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53345-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53345-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53345-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53345-135">입력</span><span class="sxs-lookup"><span data-stu-id="53345-135">INPUTS</span></span>

### <span data-ttu-id="53345-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53345-136">System.String</span></span>

## <span data-ttu-id="53345-137">출력</span><span class="sxs-lookup"><span data-stu-id="53345-137">OUTPUTS</span></span>

### <span data-ttu-id="53345-138">Update.exe. PSApplyUpdate.</span><span class="sxs-lookup"><span data-stu-id="53345-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="53345-139">상속자</span><span class="sxs-lookup"><span data-stu-id="53345-139">NOTES</span></span>

## <span data-ttu-id="53345-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53345-140">RELATED LINKS</span></span>
