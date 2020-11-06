---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 3f139d4164c092f6ef57ad29d5ab9ad3eac59b56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533408"
---
# <span data-ttu-id="4ba21-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ba21-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4ba21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba21-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba21-103">계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ba21-104">SYNTAX</span></span>

### <span data-ttu-id="4ba21-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba21-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ba21-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ba21-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ba21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ba21-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba21-108">**AzureRmCognitiveServicesAccount** Cmdlet은 *ResoureGroupName* 매개 변수에 지정 된 리소스 그룹에서 프로 비전 된 인식 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>
<span data-ttu-id="4ba21-109">*ResoureGroupName* 매개 변수를 지정 하지 않으면이 cmdlet은 현재 구독에 대 한 모든 인식 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="4ba21-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4ba21-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba21-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ba21-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="4ba21-112">변수</span><span class="sxs-lookup"><span data-stu-id="4ba21-112">PARAMETERS</span></span>

### <span data-ttu-id="4ba21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba21-113">-DefaultProfile</span></span>
<span data-ttu-id="4ba21-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ba21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ba21-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4ba21-115">-Name</span></span>
<span data-ttu-id="4ba21-116">가져올 인식 서비스 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba21-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ba21-118">인지 서비스 계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba21-119">CommonParameters</span></span>
<span data-ttu-id="4ba21-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba21-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba21-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba21-122">입력</span><span class="sxs-lookup"><span data-stu-id="4ba21-122">INPUTS</span></span>

### <span data-ttu-id="4ba21-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ba21-123">System.String</span></span>

## <span data-ttu-id="4ba21-124">출력</span><span class="sxs-lookup"><span data-stu-id="4ba21-124">OUTPUTS</span></span>

### <span data-ttu-id="4ba21-125">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="4ba21-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4ba21-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4ba21-126">NOTES</span></span>

## <span data-ttu-id="4ba21-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ba21-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ba21-128">새로운 AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ba21-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4ba21-129">제거-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ba21-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4ba21-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ba21-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


