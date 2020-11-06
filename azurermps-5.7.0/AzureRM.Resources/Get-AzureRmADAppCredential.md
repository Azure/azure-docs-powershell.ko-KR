---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529732"
---
# <span data-ttu-id="9e90f-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e90f-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="9e90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e90f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e90f-103">응용 프로그램과 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e90f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e90f-104">SYNTAX</span></span>

### <span data-ttu-id="9e90f-105">ApplicationObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e90f-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e90f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e90f-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e90f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e90f-107">DESCRIPTION</span></span>
<span data-ttu-id="9e90f-108">Get-AzureRmADAppCredential cmdlet을 사용 하 여 응용 프로그램과 연결 된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="9e90f-109">이 명령은 응용 프로그램과 연결 된 자격 증명 속성 (자격 증명 값 제외)을 모두 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="9e90f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9e90f-110">EXAMPLES</span></span>

### <span data-ttu-id="9e90f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e90f-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="9e90f-112">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램과 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="9e90f-113">변수</span><span class="sxs-lookup"><span data-stu-id="9e90f-113">PARAMETERS</span></span>

### <span data-ttu-id="9e90f-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9e90f-114">-ApplicationId</span></span>
<span data-ttu-id="9e90f-115">자격 증명을 검색할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e90f-116">-DefaultProfile</span></span>
<span data-ttu-id="9e90f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e90f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e90f-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9e90f-118">-ObjectId</span></span>
<span data-ttu-id="9e90f-119">자격 증명을 검색할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e90f-120">CommonParameters</span></span>
<span data-ttu-id="9e90f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e90f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e90f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e90f-123">입력</span><span class="sxs-lookup"><span data-stu-id="9e90f-123">INPUTS</span></span>

### <span data-ttu-id="9e90f-124">않아야</span><span class="sxs-lookup"><span data-stu-id="9e90f-124">None</span></span>
<span data-ttu-id="9e90f-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e90f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e90f-126">출력</span><span class="sxs-lookup"><span data-stu-id="9e90f-126">OUTPUTS</span></span>

### <span data-ttu-id="9e90f-127">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="9e90f-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9e90f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9e90f-128">NOTES</span></span>

## <span data-ttu-id="9e90f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e90f-129">RELATED LINKS</span></span>

[<span data-ttu-id="9e90f-130">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e90f-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="9e90f-131">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9e90f-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="9e90f-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="9e90f-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

