---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533404"
---
# <span data-ttu-id="94999-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="94999-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="94999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94999-102">SYNOPSIS</span></span>
<span data-ttu-id="94999-103">사용할 수 있는 인식 서비스 계정 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94999-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94999-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94999-104">SYNTAX</span></span>

### <span data-ttu-id="94999-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="94999-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94999-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="94999-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94999-107">설명은</span><span class="sxs-lookup"><span data-stu-id="94999-107">DESCRIPTION</span></span>
<span data-ttu-id="94999-108">**AzureRmCognitiveServicesAccountType** cmdlet은이 구독에서 사용 가능한 인식 서비스 계정 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94999-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="94999-109">예제의</span><span class="sxs-lookup"><span data-stu-id="94999-109">EXAMPLES</span></span>

### <span data-ttu-id="94999-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="94999-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="94999-111">사용 가능한 형식 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94999-111">Get the list of available Types.</span></span>

### <span data-ttu-id="94999-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="94999-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="94999-113">Westus에서 사용 가능한 형식 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94999-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="94999-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="94999-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="94999-115">유효한 `Face` 형식 이름 인지 확인 하 고 올바른 이름인 경우 이름이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94999-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="94999-116">변수</span><span class="sxs-lookup"><span data-stu-id="94999-116">PARAMETERS</span></span>

### <span data-ttu-id="94999-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94999-117">-DefaultProfile</span></span>
<span data-ttu-id="94999-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94999-119">-위치</span><span class="sxs-lookup"><span data-stu-id="94999-119">-Location</span></span>
<span data-ttu-id="94999-120">인식 서비스 계정 위치.</span><span class="sxs-lookup"><span data-stu-id="94999-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="94999-121">-TypeName</span></span>
<span data-ttu-id="94999-122">인식 서비스 계정 유형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94999-123">CommonParameters</span></span>
<span data-ttu-id="94999-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94999-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94999-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94999-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94999-126">입력</span><span class="sxs-lookup"><span data-stu-id="94999-126">INPUTS</span></span>

### <span data-ttu-id="94999-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94999-127">System.String</span></span>

## <span data-ttu-id="94999-128">출력</span><span class="sxs-lookup"><span data-stu-id="94999-128">OUTPUTS</span></span>

### <span data-ttu-id="94999-129">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="94999-129">System.String[]</span></span>

### <span data-ttu-id="94999-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94999-130">System.String</span></span>

## <span data-ttu-id="94999-131">상속자</span><span class="sxs-lookup"><span data-stu-id="94999-131">NOTES</span></span>

## <span data-ttu-id="94999-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94999-132">RELATED LINKS</span></span>
