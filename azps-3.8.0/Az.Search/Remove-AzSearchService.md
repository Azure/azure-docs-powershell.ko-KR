---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043493"
---
# <span data-ttu-id="7d1fb-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d1fb-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="7d1fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1fb-103">Azure Search service를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="7d1fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d1fb-104">SYNTAX</span></span>

### <span data-ttu-id="7d1fb-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1fb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1fb-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1fb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1fb-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1fb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7d1fb-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1fb-109">**AzSearchService** cmdlet은 지정 된 매개 변수를 사용 하 여 Azure Search 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="7d1fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7d1fb-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d1fb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="7d1fb-112">이 예제에서는 Azure Search 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="7d1fb-113">변수</span><span class="sxs-lookup"><span data-stu-id="7d1fb-113">PARAMETERS</span></span>

### <span data-ttu-id="7d1fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1fb-114">-DefaultProfile</span></span>
<span data-ttu-id="7d1fb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d1fb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7d1fb-116">-Force</span></span>
<span data-ttu-id="7d1fb-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7d1fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d1fb-118">-InputObject</span></span>
<span data-ttu-id="7d1fb-119">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1fb-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7d1fb-120">-Name</span></span>
<span data-ttu-id="7d1fb-121">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-121">Search Service name.</span></span>

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

### <span data-ttu-id="7d1fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d1fb-122">-PassThru</span></span>
<span data-ttu-id="7d1fb-123">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7d1fb-124">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7d1fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d1fb-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-126">Resource Group name.</span></span>

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

### <span data-ttu-id="7d1fb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1fb-127">-ResourceId</span></span>
<span data-ttu-id="7d1fb-128">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1fb-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7d1fb-129">-Confirm</span></span>
<span data-ttu-id="7d1fb-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1fb-131">-WhatIf</span></span>
<span data-ttu-id="7d1fb-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1fb-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1fb-134">CommonParameters</span></span>
<span data-ttu-id="7d1fb-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1fb-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1fb-137">입력</span><span class="sxs-lookup"><span data-stu-id="7d1fb-137">INPUTS</span></span>

### <span data-ttu-id="7d1fb-138">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7d1fb-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d1fb-139">System.String</span></span>

## <span data-ttu-id="7d1fb-140">출력</span><span class="sxs-lookup"><span data-stu-id="7d1fb-140">OUTPUTS</span></span>

### <span data-ttu-id="7d1fb-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7d1fb-141">System.Boolean</span></span>

## <span data-ttu-id="7d1fb-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7d1fb-142">NOTES</span></span>

## <span data-ttu-id="7d1fb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d1fb-143">RELATED LINKS</span></span>

[<span data-ttu-id="7d1fb-144">새로운 AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d1fb-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="7d1fb-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d1fb-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7d1fb-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d1fb-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

