---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ddc47a08c7042b61bd77433adb8a10a7f39e8f00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699278"
---
# <span data-ttu-id="f9085-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="f9085-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="f9085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9085-102">SYNOPSIS</span></span>
<span data-ttu-id="f9085-103">Azure Search 서비스의 관리자 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="f9085-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9085-104">SYNTAX</span></span>

### <span data-ttu-id="f9085-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9085-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9085-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9085-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9085-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9085-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9085-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f9085-108">DESCRIPTION</span></span>
<span data-ttu-id="f9085-109">**AzSearchAdminKey** Cmdlet은 Azure Search 서비스의 관리자 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="f9085-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f9085-110">EXAMPLES</span></span>

### <span data-ttu-id="f9085-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9085-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="f9085-112">이 예제에서는 Azure Search 서비스의 기본 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="f9085-113">변수</span><span class="sxs-lookup"><span data-stu-id="f9085-113">PARAMETERS</span></span>

### <span data-ttu-id="f9085-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9085-114">-DefaultProfile</span></span>
<span data-ttu-id="f9085-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9085-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f9085-116">-Force</span></span>
<span data-ttu-id="f9085-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9085-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="f9085-118">-KeyKind</span></span>
<span data-ttu-id="f9085-119">Search Service 관리 키 종류 (기본/보조).</span><span class="sxs-lookup"><span data-stu-id="f9085-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="f9085-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f9085-120">-ParentObject</span></span>
<span data-ttu-id="f9085-121">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="f9085-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f9085-122">-ParentResourceId</span></span>
<span data-ttu-id="f9085-123">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="f9085-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9085-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9085-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-125">Resource Group name.</span></span>

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

### <span data-ttu-id="f9085-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f9085-126">-ServiceName</span></span>
<span data-ttu-id="f9085-127">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-127">Search Service name.</span></span>

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

### <span data-ttu-id="f9085-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f9085-128">-Confirm</span></span>
<span data-ttu-id="f9085-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9085-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9085-130">-WhatIf</span></span>
<span data-ttu-id="f9085-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9085-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9085-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9085-133">CommonParameters</span></span>
<span data-ttu-id="f9085-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9085-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9085-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9085-136">입력</span><span class="sxs-lookup"><span data-stu-id="f9085-136">INPUTS</span></span>

### <span data-ttu-id="f9085-137">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f9085-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9085-138">System.String</span></span>

## <span data-ttu-id="f9085-139">출력</span><span class="sxs-lookup"><span data-stu-id="f9085-139">OUTPUTS</span></span>

### <span data-ttu-id="f9085-140">. PSSearchAdminKey를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9085-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="f9085-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f9085-141">NOTES</span></span>

## <span data-ttu-id="f9085-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9085-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9085-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="f9085-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
