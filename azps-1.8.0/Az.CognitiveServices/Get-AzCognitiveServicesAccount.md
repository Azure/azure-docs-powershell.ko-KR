---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5488e3df4b4404986f2e4252b534e3bff4f6f6df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869189"
---
# <span data-ttu-id="64d88-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="64d88-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="64d88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d88-102">SYNOPSIS</span></span>
<span data-ttu-id="64d88-103">계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-103">Gets an account.</span></span>

## <span data-ttu-id="64d88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64d88-104">SYNTAX</span></span>

### <span data-ttu-id="64d88-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d88-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64d88-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d88-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d88-107">설명은</span><span class="sxs-lookup"><span data-stu-id="64d88-107">DESCRIPTION</span></span>
<span data-ttu-id="64d88-108">**AzCognitiveServicesAccount** Cmdlet은 *ResoureGroupName* 매개 변수에 지정 된 리소스 그룹에서 프로 비전 된 인식 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>
<span data-ttu-id="64d88-109">*ResoureGroupName* 매개 변수를 지정 하지 않으면이 cmdlet은 현재 구독에 대 한 모든 인식 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="64d88-110">예제의</span><span class="sxs-lookup"><span data-stu-id="64d88-110">EXAMPLES</span></span>

### <span data-ttu-id="64d88-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="64d88-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
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

## <span data-ttu-id="64d88-112">변수</span><span class="sxs-lookup"><span data-stu-id="64d88-112">PARAMETERS</span></span>

### <span data-ttu-id="64d88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d88-113">-DefaultProfile</span></span>
<span data-ttu-id="64d88-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="64d88-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64d88-115">-이름</span><span class="sxs-lookup"><span data-stu-id="64d88-115">-Name</span></span>
<span data-ttu-id="64d88-116">가져올 인식 서비스 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="64d88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d88-117">-ResourceGroupName</span></span>
<span data-ttu-id="64d88-118">인지 서비스 계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="64d88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d88-119">CommonParameters</span></span>
<span data-ttu-id="64d88-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d88-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d88-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d88-122">입력</span><span class="sxs-lookup"><span data-stu-id="64d88-122">INPUTS</span></span>

### <span data-ttu-id="64d88-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64d88-123">System.String</span></span>

## <span data-ttu-id="64d88-124">출력</span><span class="sxs-lookup"><span data-stu-id="64d88-124">OUTPUTS</span></span>

### <span data-ttu-id="64d88-125">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="64d88-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="64d88-126">상속자</span><span class="sxs-lookup"><span data-stu-id="64d88-126">NOTES</span></span>

## <span data-ttu-id="64d88-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64d88-127">RELATED LINKS</span></span>

[<span data-ttu-id="64d88-128">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="64d88-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="64d88-129">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="64d88-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="64d88-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="64d88-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


