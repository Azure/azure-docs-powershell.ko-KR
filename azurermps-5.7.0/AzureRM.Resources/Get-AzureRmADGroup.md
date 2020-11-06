---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533659"
---
# <span data-ttu-id="d62f5-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="d62f5-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="d62f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d62f5-103">Active directory 그룹을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d62f5-104">SYNTAX</span></span>

### <span data-ttu-id="d62f5-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d62f5-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d62f5-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d62f5-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d62f5-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d62f5-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d62f5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d62f5-108">DESCRIPTION</span></span>
<span data-ttu-id="d62f5-109">Active directory 그룹을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-109">Filters active directory groups.</span></span>

## <span data-ttu-id="d62f5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d62f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d62f5-111">개체 id를 사용 하 여 그룹 필터링</span><span class="sxs-lookup"><span data-stu-id="d62f5-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d62f5-112">85F89C90-780E-4AA6-9F4F-6F268D322EEE id를 사용 하 여 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="d62f5-113">검색 문자열을 사용 하 여 그룹 필터링</span><span class="sxs-lookup"><span data-stu-id="d62f5-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="d62f5-114">표시 이름에 Joe가 있는 모든 광고 그룹을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="d62f5-115">광고 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="d62f5-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="d62f5-116">모든 광고 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-116">Gets all AD groups</span></span>

## <span data-ttu-id="d62f5-117">변수</span><span class="sxs-lookup"><span data-stu-id="d62f5-117">PARAMETERS</span></span>

### <span data-ttu-id="d62f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62f5-118">-DefaultProfile</span></span>
<span data-ttu-id="d62f5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d62f5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62f5-120">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d62f5-120">-ObjectId</span></span>
<span data-ttu-id="d62f5-121">그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62f5-122">-SearchString</span><span class="sxs-lookup"><span data-stu-id="d62f5-122">-SearchString</span></span>
<span data-ttu-id="d62f5-123">그룹 표시 이름</span><span class="sxs-lookup"><span data-stu-id="d62f5-123">The group display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62f5-124">CommonParameters</span></span>
<span data-ttu-id="d62f5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62f5-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62f5-127">입력</span><span class="sxs-lookup"><span data-stu-id="d62f5-127">INPUTS</span></span>

### <span data-ttu-id="d62f5-128">않아야</span><span class="sxs-lookup"><span data-stu-id="d62f5-128">None</span></span>
<span data-ttu-id="d62f5-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d62f5-130">출력</span><span class="sxs-lookup"><span data-stu-id="d62f5-130">OUTPUTS</span></span>

### <span data-ttu-id="d62f5-131">ActiveDirectory의 ' 1 Microsoft.Azure.Graph.RBAC.Version1_6 [PSADGroup] 목록</span><span class="sxs-lookup"><span data-stu-id="d62f5-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="d62f5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d62f5-132">NOTES</span></span>

## <span data-ttu-id="d62f5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d62f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="d62f5-134">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d62f5-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="d62f5-135">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d62f5-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d62f5-136">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="d62f5-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

