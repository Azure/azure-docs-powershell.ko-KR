---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212557"
---
# <span data-ttu-id="a87d4-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="a87d4-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="a87d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a87d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a87d4-103">연결을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-103">Create or update an association.</span></span>

## <span data-ttu-id="a87d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a87d4-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a87d4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a87d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a87d4-106">연결을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-106">Create or update an association.</span></span>

## <span data-ttu-id="a87d4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a87d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a87d4-108">예제 1: 사용자 지정 공급자 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="a87d4-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="a87d4-109">사용자 지정 공급자 연결 만들기 "연결"에 대 한 경로를 사용 하 여 연결 된 대상에 대 한 경로가 올바르게 구성 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="a87d4-110">변수</span><span class="sxs-lookup"><span data-stu-id="a87d4-110">PARAMETERS</span></span>

### <span data-ttu-id="a87d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a87d4-111">-AsJob</span></span>
<span data-ttu-id="a87d4-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a87d4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a87d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87d4-113">-DefaultProfile</span></span>
<span data-ttu-id="a87d4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a87d4-115">-Name</span></span>
<span data-ttu-id="a87d4-116">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d4-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a87d4-117">-NoWait</span></span>
<span data-ttu-id="a87d4-118">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a87d4-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a87d4-119">-범위</span><span class="sxs-lookup"><span data-stu-id="a87d4-119">-Scope</span></span>
<span data-ttu-id="a87d4-120">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-120">The scope of the association.</span></span>
<span data-ttu-id="a87d4-121">범위는 유효한 REST 리소스 인스턴스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="a87d4-122">예를 들어 가상 컴퓨터 리소스에는 '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name} '을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d4-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a87d4-123">-TargetResourceId</span></span>
<span data-ttu-id="a87d4-124">이 연결에 대 한 대상 리소스의 REST 리소스 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="a87d4-125">-확인</span><span class="sxs-lookup"><span data-stu-id="a87d4-125">-Confirm</span></span>
<span data-ttu-id="a87d4-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a87d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87d4-127">-WhatIf</span></span>
<span data-ttu-id="a87d4-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a87d4-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a87d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87d4-130">CommonParameters</span></span>
<span data-ttu-id="a87d4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a87d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87d4-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a87d4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87d4-133">입력</span><span class="sxs-lookup"><span data-stu-id="a87d4-133">INPUTS</span></span>

## <span data-ttu-id="a87d4-134">출력</span><span class="sxs-lookup"><span data-stu-id="a87d4-134">OUTPUTS</span></span>

### <span data-ttu-id="a87d4-135">Api20180901Preview 연결을 위한. i i m.</span><span class="sxs-lookup"><span data-stu-id="a87d4-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="a87d4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a87d4-136">NOTES</span></span>

<span data-ttu-id="a87d4-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="a87d4-137">ALIASES</span></span>

## <span data-ttu-id="a87d4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a87d4-138">RELATED LINKS</span></span>

