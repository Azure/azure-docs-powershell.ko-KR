---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537000"
---
# <span data-ttu-id="d0619-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d0619-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="d0619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0619-102">SYNOPSIS</span></span>
<span data-ttu-id="d0619-103">응용 프로그램과 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0619-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0619-104">SYNTAX</span></span>

### <span data-ttu-id="d0619-105">ApplicationObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0619-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0619-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0619-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0619-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d0619-107">DESCRIPTION</span></span>
<span data-ttu-id="d0619-108">Get-AzureRmADAppCredential cmdlet을 사용 하 여 응용 프로그램과 연결 된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="d0619-109">이 명령은 응용 프로그램과 연결 된 자격 증명 속성 (자격 증명 값 제외)을 모두 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="d0619-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d0619-110">EXAMPLES</span></span>

### <span data-ttu-id="d0619-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0619-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="d0619-112">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램과 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="d0619-113">변수</span><span class="sxs-lookup"><span data-stu-id="d0619-113">PARAMETERS</span></span>

### <span data-ttu-id="d0619-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d0619-114">-ApplicationId</span></span>
<span data-ttu-id="d0619-115">자격 증명을 검색할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0619-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d0619-116">-ObjectId</span></span>
<span data-ttu-id="d0619-117">자격 증명을 검색할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0619-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0619-118">-DefaultProfile</span></span>
<span data-ttu-id="d0619-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0619-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0619-120">CommonParameters</span></span>
<span data-ttu-id="d0619-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0619-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0619-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0619-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0619-123">입력</span><span class="sxs-lookup"><span data-stu-id="d0619-123">INPUTS</span></span>

## <span data-ttu-id="d0619-124">출력</span><span class="sxs-lookup"><span data-stu-id="d0619-124">OUTPUTS</span></span>

### <span data-ttu-id="d0619-125">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="d0619-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="d0619-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d0619-126">NOTES</span></span>

## <span data-ttu-id="d0619-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0619-127">RELATED LINKS</span></span>

[<span data-ttu-id="d0619-128">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d0619-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="d0619-129">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d0619-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="d0619-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d0619-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

