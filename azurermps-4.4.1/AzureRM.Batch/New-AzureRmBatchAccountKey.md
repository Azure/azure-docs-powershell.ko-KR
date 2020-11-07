---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: fbfcbaa0fdf790daad05aece6190396c735f9fff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702772"
---
# <span data-ttu-id="96459-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="96459-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="96459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96459-102">SYNOPSIS</span></span>
<span data-ttu-id="96459-103">일괄 처리 계정의 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96459-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96459-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96459-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96459-105">DESCRIPTION</span></span>
<span data-ttu-id="96459-106">**AzureRmBatchAccountKey** Cmdlet은 Azure Batch 계정의 기본 또는 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="96459-107">Cmdlet은 현재 **PrimaryAccountKey** 및 **SecondaryAccountKey** 속성이 있는 **batchaccountcontext** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="96459-108">예제의</span><span class="sxs-lookup"><span data-stu-id="96459-108">EXAMPLES</span></span>

### <span data-ttu-id="96459-109">예제 1: 일괄 처리 계정에서 기본 계정 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="96459-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="96459-110">이 명령은 pfuller 라는 일괄 계정에서 기본 계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="96459-111">변수</span><span class="sxs-lookup"><span data-stu-id="96459-111">PARAMETERS</span></span>

### <span data-ttu-id="96459-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96459-112">-AccountName</span></span>
<span data-ttu-id="96459-113">이 cmdlet이 키를 다시 생성 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="96459-114">-KeyType</span><span class="sxs-lookup"><span data-stu-id="96459-114">-KeyType</span></span>
<span data-ttu-id="96459-115">이 cmdlet이 다시 생성 하는 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-115">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="96459-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96459-116">Valid values are:</span></span> 

- <span data-ttu-id="96459-117">주요한</span><span class="sxs-lookup"><span data-stu-id="96459-117">Primary</span></span>
- <span data-ttu-id="96459-118">보조</span><span class="sxs-lookup"><span data-stu-id="96459-118">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96459-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96459-119">-ResourceGroupName</span></span>
<span data-ttu-id="96459-120">이 cmdlet이 키를 다시 생성 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-120">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="96459-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96459-121">-DefaultProfile</span></span>
<span data-ttu-id="96459-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96459-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96459-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96459-123">CommonParameters</span></span>
<span data-ttu-id="96459-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96459-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96459-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96459-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96459-126">입력</span><span class="sxs-lookup"><span data-stu-id="96459-126">INPUTS</span></span>

## <span data-ttu-id="96459-127">출력</span><span class="sxs-lookup"><span data-stu-id="96459-127">OUTPUTS</span></span>

### <span data-ttu-id="96459-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96459-128">BatchAccountContext</span></span>

## <span data-ttu-id="96459-129">상속자</span><span class="sxs-lookup"><span data-stu-id="96459-129">NOTES</span></span>

## <span data-ttu-id="96459-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96459-130">RELATED LINKS</span></span>

[<span data-ttu-id="96459-131">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="96459-131">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="96459-132">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96459-132">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


