---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042123"
---
# <span data-ttu-id="2c9a5-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="2c9a5-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="2c9a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9a5-103">사용할 수 있는 인식 서비스 계정 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="2c9a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c9a5-104">SYNTAX</span></span>

### <span data-ttu-id="2c9a5-105">GetAccountTypes (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c9a5-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c9a5-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="2c9a5-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c9a5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c9a5-107">DESCRIPTION</span></span>
<span data-ttu-id="2c9a5-108">**AzCognitiveServicesAccountType** cmdlet은이 구독에서 사용 가능한 인식 서비스 계정 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="2c9a5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2c9a5-109">EXAMPLES</span></span>

### <span data-ttu-id="2c9a5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c9a5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="2c9a5-111">사용 가능한 형식 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-111">Get the list of available Types.</span></span>

### <span data-ttu-id="2c9a5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c9a5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="2c9a5-113">Westus에서 사용 가능한 형식 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="2c9a5-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="2c9a5-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="2c9a5-115">유효한 `Face` 형식 이름 인지 확인 하 고 올바른 이름인 경우 이름이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="2c9a5-116">변수</span><span class="sxs-lookup"><span data-stu-id="2c9a5-116">PARAMETERS</span></span>

### <span data-ttu-id="2c9a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9a5-117">-DefaultProfile</span></span>
<span data-ttu-id="2c9a5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c9a5-119">-위치</span><span class="sxs-lookup"><span data-stu-id="2c9a5-119">-Location</span></span>
<span data-ttu-id="2c9a5-120">인식 서비스 계정 위치.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="2c9a5-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="2c9a5-121">-TypeName</span></span>
<span data-ttu-id="2c9a5-122">인식 서비스 계정 유형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="2c9a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9a5-123">CommonParameters</span></span>
<span data-ttu-id="2c9a5-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9a5-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c9a5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9a5-126">입력</span><span class="sxs-lookup"><span data-stu-id="2c9a5-126">INPUTS</span></span>

### <span data-ttu-id="2c9a5-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c9a5-127">System.String</span></span>

## <span data-ttu-id="2c9a5-128">출력</span><span class="sxs-lookup"><span data-stu-id="2c9a5-128">OUTPUTS</span></span>

### <span data-ttu-id="2c9a5-129">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2c9a5-129">System.String[]</span></span>

### <span data-ttu-id="2c9a5-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c9a5-130">System.String</span></span>

## <span data-ttu-id="2c9a5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2c9a5-131">NOTES</span></span>

## <span data-ttu-id="2c9a5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c9a5-132">RELATED LINKS</span></span>