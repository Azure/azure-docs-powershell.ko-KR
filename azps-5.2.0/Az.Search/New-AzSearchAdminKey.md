---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331070"
---
# <span data-ttu-id="ca184-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="ca184-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="ca184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca184-102">SYNOPSIS</span></span>
<span data-ttu-id="ca184-103">Azure Search 서비스의 관리자 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="ca184-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca184-104">SYNTAX</span></span>

### <span data-ttu-id="ca184-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca184-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca184-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca184-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca184-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca184-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca184-108">설명</span><span class="sxs-lookup"><span data-stu-id="ca184-108">DESCRIPTION</span></span>
<span data-ttu-id="ca184-109">**New-AzSearchAdminKey** cmdlet은 Azure Search 서비스의 관리 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="ca184-110">예제</span><span class="sxs-lookup"><span data-stu-id="ca184-110">EXAMPLES</span></span>

### <span data-ttu-id="ca184-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca184-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="ca184-112">이 예제에서는 Azure Search 서비스의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="ca184-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca184-113">PARAMETERS</span></span>

### <span data-ttu-id="ca184-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca184-114">-DefaultProfile</span></span>
<span data-ttu-id="ca184-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca184-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ca184-116">-Force</span></span>
<span data-ttu-id="ca184-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ca184-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="ca184-118">-KeyKind</span></span>
<span data-ttu-id="ca184-119">Search 서비스 관리자 키 종류(기본/보조)</span><span class="sxs-lookup"><span data-stu-id="ca184-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca184-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca184-120">-ParentObject</span></span>
<span data-ttu-id="ca184-121">Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca184-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca184-122">-ParentResourceId</span></span>
<span data-ttu-id="ca184-123">Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca184-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca184-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca184-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca184-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca184-126">-ServiceName</span></span>
<span data-ttu-id="ca184-127">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-127">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca184-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca184-128">-Confirm</span></span>
<span data-ttu-id="ca184-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca184-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca184-130">-WhatIf</span></span>
<span data-ttu-id="ca184-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ca184-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca184-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca184-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca184-133">CommonParameters</span></span>
<span data-ttu-id="ca184-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca184-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca184-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca184-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca184-136">입력</span><span class="sxs-lookup"><span data-stu-id="ca184-136">INPUTS</span></span>

### <span data-ttu-id="ca184-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ca184-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ca184-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ca184-138">System.String</span></span>

## <span data-ttu-id="ca184-139">출력</span><span class="sxs-lookup"><span data-stu-id="ca184-139">OUTPUTS</span></span>

### <span data-ttu-id="ca184-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="ca184-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="ca184-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca184-141">NOTES</span></span>

## <span data-ttu-id="ca184-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca184-142">RELATED LINKS</span></span>

[<span data-ttu-id="ca184-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="ca184-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
