---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211657"
---
# <span data-ttu-id="c8b41-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="c8b41-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="c8b41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b41-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b41-103">리소스에 대 한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="c8b41-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c8b41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8b41-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8b41-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b41-106">리소스에 대 한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="c8b41-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c8b41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c8b41-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b41-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8b41-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="c8b41-109">리소스에 대 한 유지 관리 업데이트 추적</span><span class="sxs-lookup"><span data-stu-id="c8b41-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c8b41-110">변수</span><span class="sxs-lookup"><span data-stu-id="c8b41-110">PARAMETERS</span></span>

### <span data-ttu-id="c8b41-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="c8b41-111">-ApplyUpdateName</span></span>
<span data-ttu-id="c8b41-112">업데이트 적용 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b41-113">-DefaultProfile</span></span>
<span data-ttu-id="c8b41-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8b41-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c8b41-115">-ProviderName</span></span>
<span data-ttu-id="c8b41-116">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="c8b41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b41-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8b41-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="c8b41-119">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="c8b41-119">-ResourceName</span></span>
<span data-ttu-id="c8b41-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-120">The resource name.</span></span>

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

### <span data-ttu-id="c8b41-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="c8b41-121">-ResourceParentName</span></span>
<span data-ttu-id="c8b41-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-122">The parent resource name.</span></span>

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

### <span data-ttu-id="c8b41-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="c8b41-123">-ResourceParentType</span></span>
<span data-ttu-id="c8b41-124">부모 리소스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-124">The parent resource type.</span></span>

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

### <span data-ttu-id="c8b41-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c8b41-125">-ResourceType</span></span>
<span data-ttu-id="c8b41-126">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-126">The resource type.</span></span>

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

### <span data-ttu-id="c8b41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b41-127">CommonParameters</span></span>
<span data-ttu-id="c8b41-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8b41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b41-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8b41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b41-130">입력</span><span class="sxs-lookup"><span data-stu-id="c8b41-130">INPUTS</span></span>

### <span data-ttu-id="c8b41-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c8b41-131">System.String</span></span>

## <span data-ttu-id="c8b41-132">출력</span><span class="sxs-lookup"><span data-stu-id="c8b41-132">OUTPUTS</span></span>

### <span data-ttu-id="c8b41-133">Update.exe. PSApplyUpdate.</span><span class="sxs-lookup"><span data-stu-id="c8b41-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="c8b41-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c8b41-134">NOTES</span></span>

## <span data-ttu-id="c8b41-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8b41-135">RELATED LINKS</span></span>
