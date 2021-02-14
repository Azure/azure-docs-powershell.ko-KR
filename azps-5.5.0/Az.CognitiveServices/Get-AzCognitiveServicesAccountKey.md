---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195097"
---
# <span data-ttu-id="5bfd9-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5bfd9-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="5bfd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bfd9-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfd9-103">계정에 대한 API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="5bfd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bfd9-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bfd9-105">설명</span><span class="sxs-lookup"><span data-stu-id="5bfd9-105">DESCRIPTION</span></span>
<span data-ttu-id="5bfd9-106">**Get-AzCognitiveServicesAccountKey** cmdlet은 프로비전된 Cognitive Services 계정에 대한 API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="5bfd9-107">Cognitive Services 계정에는 Key1 및 Key2의 두 개의 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="5bfd9-108">키를 사용하면 Cognitive Services 계정 엔드포인트와 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="5bfd9-109">키를 New-AzCognitiveServicesAccountKey 키를 다시 생성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="5bfd9-110">예제</span><span class="sxs-lookup"><span data-stu-id="5bfd9-110">EXAMPLES</span></span>

### <span data-ttu-id="5bfd9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bfd9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="5bfd9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bfd9-112">PARAMETERS</span></span>

### <span data-ttu-id="5bfd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfd9-113">-DefaultProfile</span></span>
<span data-ttu-id="5bfd9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5bfd9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bfd9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5bfd9-115">-Name</span></span>
<span data-ttu-id="5bfd9-116">계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-116">Specifies the name of the account.</span></span>
<span data-ttu-id="5bfd9-117">이 cmdlet은 이 계정에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="5bfd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bfd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bfd9-119">계정이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="5bfd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfd9-120">CommonParameters</span></span>
<span data-ttu-id="5bfd9-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfd9-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfd9-123">입력</span><span class="sxs-lookup"><span data-stu-id="5bfd9-123">INPUTS</span></span>

### <span data-ttu-id="5bfd9-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5bfd9-124">System.String</span></span>

## <span data-ttu-id="5bfd9-125">출력</span><span class="sxs-lookup"><span data-stu-id="5bfd9-125">OUTPUTS</span></span>

### <span data-ttu-id="5bfd9-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5bfd9-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="5bfd9-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bfd9-127">NOTES</span></span>

## <span data-ttu-id="5bfd9-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bfd9-128">RELATED LINKS</span></span>

[<span data-ttu-id="5bfd9-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5bfd9-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


