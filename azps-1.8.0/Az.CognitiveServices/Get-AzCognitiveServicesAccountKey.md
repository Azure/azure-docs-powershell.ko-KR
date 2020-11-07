---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 11285a805444c270740d7158f66aa538fecfa1b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701391"
---
# <span data-ttu-id="4bc91-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="4bc91-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="4bc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc91-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc91-103">계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="4bc91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bc91-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc91-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bc91-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc91-106">**AzCognitiveServicesAccountKey** cmdlet은 프로 비전 된 인식 서비스 계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="4bc91-107">인지 서비스 계정에는 Key1 및 Key2의 두 가지 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="4bc91-108">키를 사용 하면 인식 서비스 계정 끝점과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="4bc91-109">New-AzCognitiveServicesAccountKey를 사용 하 여 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="4bc91-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4bc91-110">EXAMPLES</span></span>

### <span data-ttu-id="4bc91-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bc91-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="4bc91-112">변수</span><span class="sxs-lookup"><span data-stu-id="4bc91-112">PARAMETERS</span></span>

### <span data-ttu-id="4bc91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc91-113">-DefaultProfile</span></span>
<span data-ttu-id="4bc91-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4bc91-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bc91-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4bc91-115">-Name</span></span>
<span data-ttu-id="4bc91-116">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-116">Specifies the name of the account.</span></span>
<span data-ttu-id="4bc91-117">이 cmdlet은이 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc91-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc91-118">-ResourceGroupName</span></span>
<span data-ttu-id="4bc91-119">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc91-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc91-120">CommonParameters</span></span>
<span data-ttu-id="4bc91-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc91-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc91-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc91-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc91-123">입력</span><span class="sxs-lookup"><span data-stu-id="4bc91-123">INPUTS</span></span>

### <span data-ttu-id="4bc91-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bc91-124">System.String</span></span>

## <span data-ttu-id="4bc91-125">출력</span><span class="sxs-lookup"><span data-stu-id="4bc91-125">OUTPUTS</span></span>

### <span data-ttu-id="4bc91-126">CognitiveServices. PSCognitiveServicesAccountKeys/. \*</span><span class="sxs-lookup"><span data-stu-id="4bc91-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="4bc91-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4bc91-127">NOTES</span></span>

## <span data-ttu-id="4bc91-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bc91-128">RELATED LINKS</span></span>

[<span data-ttu-id="4bc91-129">새로운 AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="4bc91-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


