---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704082"
---
# <span data-ttu-id="853b0-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="853b0-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="853b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="853b0-102">SYNOPSIS</span></span>
<span data-ttu-id="853b0-103">일괄 처리 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="853b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="853b0-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="853b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="853b0-105">DESCRIPTION</span></span>
<span data-ttu-id="853b0-106">**AzureRmBatchAccountKeys** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="853b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="853b0-107">EXAMPLES</span></span>

## <span data-ttu-id="853b0-108">변수</span><span class="sxs-lookup"><span data-stu-id="853b0-108">PARAMETERS</span></span>

### <span data-ttu-id="853b0-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="853b0-109">-AccountName</span></span>
<span data-ttu-id="853b0-110">이 cmdlet에서 키를 가져오는 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853b0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="853b0-111">-ResourceGroupName</span></span>
<span data-ttu-id="853b0-112">이 cmdlet에서 키를 가져오는 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="853b0-113">-DefaultProfile</span></span>
<span data-ttu-id="853b0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="853b0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853b0-115">CommonParameters</span></span>
<span data-ttu-id="853b0-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="853b0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853b0-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="853b0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853b0-118">입력</span><span class="sxs-lookup"><span data-stu-id="853b0-118">INPUTS</span></span>

## <span data-ttu-id="853b0-119">출력</span><span class="sxs-lookup"><span data-stu-id="853b0-119">OUTPUTS</span></span>

### <span data-ttu-id="853b0-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="853b0-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="853b0-121">상속자</span><span class="sxs-lookup"><span data-stu-id="853b0-121">NOTES</span></span>

## <span data-ttu-id="853b0-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="853b0-122">RELATED LINKS</span></span>

[<span data-ttu-id="853b0-123">새로운 AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="853b0-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="853b0-124">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="853b0-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


