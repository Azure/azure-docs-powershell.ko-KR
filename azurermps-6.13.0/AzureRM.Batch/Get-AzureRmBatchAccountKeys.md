---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534459"
---
# <span data-ttu-id="76c3f-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="76c3f-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="76c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="76c3f-103">일괄 처리 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76c3f-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="76c3f-106">**AzureRmBatchAccountKeys** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="76c3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="76c3f-107">EXAMPLES</span></span>

## <span data-ttu-id="76c3f-108">변수</span><span class="sxs-lookup"><span data-stu-id="76c3f-108">PARAMETERS</span></span>

### <span data-ttu-id="76c3f-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76c3f-109">-AccountName</span></span>
<span data-ttu-id="76c3f-110">이 cmdlet에서 키를 가져오는 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="76c3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c3f-111">-DefaultProfile</span></span>
<span data-ttu-id="76c3f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c3f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c3f-113">-ResourceGroupName</span></span>
<span data-ttu-id="76c3f-114">이 cmdlet에서 키를 가져오는 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="76c3f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c3f-115">CommonParameters</span></span>
<span data-ttu-id="76c3f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c3f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c3f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c3f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c3f-118">입력</span><span class="sxs-lookup"><span data-stu-id="76c3f-118">INPUTS</span></span>

### <span data-ttu-id="76c3f-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76c3f-119">System.String</span></span>

## <span data-ttu-id="76c3f-120">출력</span><span class="sxs-lookup"><span data-stu-id="76c3f-120">OUTPUTS</span></span>

### <span data-ttu-id="76c3f-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76c3f-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="76c3f-122">상속자</span><span class="sxs-lookup"><span data-stu-id="76c3f-122">NOTES</span></span>

## <span data-ttu-id="76c3f-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c3f-123">RELATED LINKS</span></span>

[<span data-ttu-id="76c3f-124">새로운 AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="76c3f-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="76c3f-125">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76c3f-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


