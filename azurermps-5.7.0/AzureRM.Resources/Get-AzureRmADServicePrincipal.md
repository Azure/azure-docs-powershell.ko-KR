---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528842"
---
# <span data-ttu-id="1a3a4-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a3a4-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="1a3a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3a4-103">Active directory 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a3a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a3a4-104">SYNTAX</span></span>

### <span data-ttu-id="1a3a4-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a3a4-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a3a4-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3a4-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a3a4-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3a4-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a3a4-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3a4-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a3a4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1a3a4-109">DESCRIPTION</span></span>
<span data-ttu-id="1a3a4-110">Active directory 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="1a3a4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1a3a4-111">EXAMPLES</span></span>

### <span data-ttu-id="1a3a4-112">SPN을 사용 하 여 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="1a3a4-113">36f81fc3-b00f-48cd51ff39f SPN을 사용 하 여 서비스 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="1a3a4-114">검색 문자열을 사용 하 여 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="1a3a4-115">표시 이름이 "Web"으로 시작 하는 모든 ad 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="1a3a4-116">광고 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="1a3a4-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="1a3a4-117">모든 광고 서비스 주체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="1a3a4-118">변수</span><span class="sxs-lookup"><span data-stu-id="1a3a4-118">PARAMETERS</span></span>

### <span data-ttu-id="1a3a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3a4-119">-DefaultProfile</span></span>
<span data-ttu-id="1a3a4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a3a4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a3a4-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1a3a4-121">-ObjectId</span></span>
<span data-ttu-id="1a3a4-122">서비스 사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-122">Object id of the service principal.</span></span>

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

### <span data-ttu-id="1a3a4-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="1a3a4-123">-SearchString</span></span>
<span data-ttu-id="1a3a4-124">표시 이름이이 값으로 시작 하는 모든 서비스 사용자를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-124">Fetches all service principals that have the display name starting with this value.</span></span>

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

### <span data-ttu-id="1a3a4-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1a3a4-125">-ServicePrincipalName</span></span>
<span data-ttu-id="1a3a4-126">서비스의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3a4-127">CommonParameters</span></span>
<span data-ttu-id="1a3a4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3a4-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a3a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3a4-130">입력</span><span class="sxs-lookup"><span data-stu-id="1a3a4-130">INPUTS</span></span>

### <span data-ttu-id="1a3a4-131">않아야</span><span class="sxs-lookup"><span data-stu-id="1a3a4-131">None</span></span>
<span data-ttu-id="1a3a4-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a3a4-133">출력</span><span class="sxs-lookup"><span data-stu-id="1a3a4-133">OUTPUTS</span></span>

### <span data-ttu-id="1a3a4-134">ActiveDirectory에서 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 목록 '을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3a4-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="1a3a4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="1a3a4-135">NOTES</span></span>

## <span data-ttu-id="1a3a4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a3a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a3a4-137">새로운 AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a3a4-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1a3a4-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a3a4-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1a3a4-139">제거-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a3a4-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1a3a4-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1a3a4-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="1a3a4-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a3a4-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

