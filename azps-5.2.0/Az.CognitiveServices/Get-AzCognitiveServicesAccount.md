---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362055"
---
# <span data-ttu-id="f328e-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f328e-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="f328e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f328e-102">SYNOPSIS</span></span>
<span data-ttu-id="f328e-103">계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-103">Gets an account.</span></span>

## <span data-ttu-id="f328e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f328e-104">SYNTAX</span></span>

### <span data-ttu-id="f328e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f328e-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f328e-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f328e-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f328e-107">설명</span><span class="sxs-lookup"><span data-stu-id="f328e-107">DESCRIPTION</span></span>
<span data-ttu-id="f328e-108">**Get-AzCognitiveServicesAccount** cmdlet은 *ResourceGroupName* 매개 변수로 지정된 리소스 그룹에서 프로비전된 Cognitive Services 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f328e-109">*ResourceGroupName* 매개 변수를 지정하지 않으면 이 cmdlet은 현재 구독에 대한 모든 Cognitive Services 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="f328e-110">예제</span><span class="sxs-lookup"><span data-stu-id="f328e-110">EXAMPLES</span></span>

### <span data-ttu-id="f328e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f328e-111">Example 1</span></span>
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

## <span data-ttu-id="f328e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f328e-112">PARAMETERS</span></span>

### <span data-ttu-id="f328e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f328e-113">-DefaultProfile</span></span>
<span data-ttu-id="f328e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f328e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f328e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f328e-115">-Name</span></span>
<span data-ttu-id="f328e-116">얻을 Cognitive Services 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="f328e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f328e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f328e-118">Cognitive Services 계정이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="f328e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f328e-119">CommonParameters</span></span>
<span data-ttu-id="f328e-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f328e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f328e-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f328e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f328e-122">입력</span><span class="sxs-lookup"><span data-stu-id="f328e-122">INPUTS</span></span>

### <span data-ttu-id="f328e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f328e-123">System.String</span></span>

## <span data-ttu-id="f328e-124">출력</span><span class="sxs-lookup"><span data-stu-id="f328e-124">OUTPUTS</span></span>

### <span data-ttu-id="f328e-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f328e-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="f328e-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f328e-126">NOTES</span></span>

## <span data-ttu-id="f328e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f328e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f328e-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f328e-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f328e-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f328e-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f328e-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f328e-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


