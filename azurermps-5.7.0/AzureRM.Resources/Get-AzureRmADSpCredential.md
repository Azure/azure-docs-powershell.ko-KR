---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702844"
---
# <span data-ttu-id="12628-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="12628-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="12628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12628-102">SYNOPSIS</span></span>
<span data-ttu-id="12628-103">서비스 사용자와 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="12628-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12628-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12628-104">SYNTAX</span></span>

### <span data-ttu-id="12628-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="12628-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12628-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="12628-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12628-107">설명은</span><span class="sxs-lookup"><span data-stu-id="12628-107">DESCRIPTION</span></span>
<span data-ttu-id="12628-108">Get-AzureRmADSpCredential cmdlet은 서비스 사용자와 연결 된 자격 증명 목록을 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12628-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="12628-109">이 명령은 서비스 사용자와 연결 된 모든 자격 증명 속성 (자격 증명 값 제외)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="12628-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="12628-110">예제의</span><span class="sxs-lookup"><span data-stu-id="12628-110">EXAMPLES</span></span>

### <span data-ttu-id="12628-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="12628-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="12628-112">SPN이 있는 서비스 사용자와 연결 된 자격 증명 목록을 반환 http://test12345 합니다.</span><span class="sxs-lookup"><span data-stu-id="12628-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="12628-113">변수</span><span class="sxs-lookup"><span data-stu-id="12628-113">PARAMETERS</span></span>

### <span data-ttu-id="12628-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12628-114">-DefaultProfile</span></span>
<span data-ttu-id="12628-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12628-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12628-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="12628-116">-ObjectId</span></span>
<span data-ttu-id="12628-117">자격 증명을 검색할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="12628-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12628-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="12628-118">-ServicePrincipalName</span></span>
<span data-ttu-id="12628-119">자격 증명을 검색할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="12628-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12628-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12628-120">CommonParameters</span></span>
<span data-ttu-id="12628-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12628-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12628-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12628-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12628-123">입력</span><span class="sxs-lookup"><span data-stu-id="12628-123">INPUTS</span></span>

### <span data-ttu-id="12628-124">않아야</span><span class="sxs-lookup"><span data-stu-id="12628-124">None</span></span>
<span data-ttu-id="12628-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12628-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12628-126">출력</span><span class="sxs-lookup"><span data-stu-id="12628-126">OUTPUTS</span></span>

### <span data-ttu-id="12628-127">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="12628-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="12628-128">상속자</span><span class="sxs-lookup"><span data-stu-id="12628-128">NOTES</span></span>

## <span data-ttu-id="12628-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12628-129">RELATED LINKS</span></span>

[<span data-ttu-id="12628-130">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="12628-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="12628-131">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="12628-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="12628-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="12628-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

