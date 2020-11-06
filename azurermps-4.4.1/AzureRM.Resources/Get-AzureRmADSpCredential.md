---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527320"
---
# <span data-ttu-id="5f98f-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f98f-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="5f98f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f98f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f98f-103">서비스 사용자와 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f98f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f98f-104">SYNTAX</span></span>

### <span data-ttu-id="5f98f-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f98f-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f98f-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f98f-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f98f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f98f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f98f-108">Get-AzureRmADSpCredential cmdlet은 서비스 사용자와 연결 된 자격 증명 목록을 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="5f98f-109">이 명령은 서비스 사용자와 연결 된 모든 자격 증명 속성 (자격 증명 값 제외)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="5f98f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5f98f-110">EXAMPLES</span></span>

### <span data-ttu-id="5f98f-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f98f-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="5f98f-112">SPN이 있는 서비스 사용자와 연결 된 자격 증명 목록을 반환 http://test12345 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="5f98f-113">변수</span><span class="sxs-lookup"><span data-stu-id="5f98f-113">PARAMETERS</span></span>

### <span data-ttu-id="5f98f-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5f98f-114">-ObjectId</span></span>
<span data-ttu-id="5f98f-115">자격 증명을 검색할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f98f-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f98f-116">-ServicePrincipalName</span></span>
<span data-ttu-id="5f98f-117">자격 증명을 검색할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f98f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f98f-118">-DefaultProfile</span></span>
<span data-ttu-id="5f98f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f98f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f98f-120">CommonParameters</span></span>
<span data-ttu-id="5f98f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f98f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f98f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f98f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f98f-123">입력</span><span class="sxs-lookup"><span data-stu-id="5f98f-123">INPUTS</span></span>

## <span data-ttu-id="5f98f-124">출력</span><span class="sxs-lookup"><span data-stu-id="5f98f-124">OUTPUTS</span></span>

### <span data-ttu-id="5f98f-125">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="5f98f-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="5f98f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5f98f-126">NOTES</span></span>

## <span data-ttu-id="5f98f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f98f-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f98f-128">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f98f-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="5f98f-129">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f98f-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="5f98f-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5f98f-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)
