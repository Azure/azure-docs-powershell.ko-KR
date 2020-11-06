---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525352"
---
# <span data-ttu-id="17d55-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="17d55-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="17d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17d55-102">SYNOPSIS</span></span>
<span data-ttu-id="17d55-103">일괄 처리 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17d55-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17d55-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17d55-105">DESCRIPTION</span></span>
<span data-ttu-id="17d55-106">**AzureRmBatchAccountKeys** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="17d55-107">예제의</span><span class="sxs-lookup"><span data-stu-id="17d55-107">EXAMPLES</span></span>

## <span data-ttu-id="17d55-108">변수</span><span class="sxs-lookup"><span data-stu-id="17d55-108">PARAMETERS</span></span>

### <span data-ttu-id="17d55-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17d55-109">-AccountName</span></span>
<span data-ttu-id="17d55-110">이 cmdlet에서 키를 가져오는 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d55-111">-DefaultProfile</span></span>
<span data-ttu-id="17d55-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17d55-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d55-113">-ResourceGroupName</span></span>
<span data-ttu-id="17d55-114">이 cmdlet에서 키를 가져오는 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d55-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d55-115">CommonParameters</span></span>
<span data-ttu-id="17d55-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d55-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d55-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d55-118">입력</span><span class="sxs-lookup"><span data-stu-id="17d55-118">INPUTS</span></span>

### <span data-ttu-id="17d55-119">않아야</span><span class="sxs-lookup"><span data-stu-id="17d55-119">None</span></span>
<span data-ttu-id="17d55-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17d55-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17d55-121">출력</span><span class="sxs-lookup"><span data-stu-id="17d55-121">OUTPUTS</span></span>

### <span data-ttu-id="17d55-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="17d55-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="17d55-123">상속자</span><span class="sxs-lookup"><span data-stu-id="17d55-123">NOTES</span></span>

## <span data-ttu-id="17d55-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17d55-124">RELATED LINKS</span></span>

[<span data-ttu-id="17d55-125">새로운 AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="17d55-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="17d55-126">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="17d55-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


