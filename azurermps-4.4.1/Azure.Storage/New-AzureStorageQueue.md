---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537939"
---
# <span data-ttu-id="e5926-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e5926-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="e5926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5926-102">SYNOPSIS</span></span>
<span data-ttu-id="e5926-103">저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5926-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5926-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e5926-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5926-105">DESCRIPTION</span></span>
<span data-ttu-id="e5926-106">**AzureStorageQueue** Cmdlet은 Azure에서 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="e5926-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5926-107">EXAMPLES</span></span>

### <span data-ttu-id="e5926-108">예제 1: Azure 저장소 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="e5926-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="e5926-109">이 예제에서는 queueabc 라는 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="e5926-110">예제 2: 여러 azure storage 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="e5926-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="e5926-111">이 예제에서는 여러 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="e5926-112">.NET 문자열 클래스의 Split 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="e5926-113">변수</span><span class="sxs-lookup"><span data-stu-id="e5926-113">PARAMETERS</span></span>

### <span data-ttu-id="e5926-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e5926-114">-Context</span></span>
<span data-ttu-id="e5926-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e5926-116">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5926-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e5926-117">-Name</span></span>
<span data-ttu-id="e5926-118">큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5926-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5926-119">CommonParameters</span></span>
<span data-ttu-id="e5926-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5926-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5926-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5926-122">입력</span><span class="sxs-lookup"><span data-stu-id="e5926-122">INPUTS</span></span>

### <span data-ttu-id="e5926-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5926-123">IStorageContext</span></span>

<span data-ttu-id="e5926-124">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e5926-125">이름</span><span class="sxs-lookup"><span data-stu-id="e5926-125">String</span></span>

<span data-ttu-id="e5926-126">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e5926-127">출력</span><span class="sxs-lookup"><span data-stu-id="e5926-127">OUTPUTS</span></span>

### <span data-ttu-id="e5926-128">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5926-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="e5926-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e5926-129">NOTES</span></span>

## <span data-ttu-id="e5926-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5926-130">RELATED LINKS</span></span>

[<span data-ttu-id="e5926-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e5926-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="e5926-132">제거-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e5926-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


