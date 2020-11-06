---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524023"
---
# <span data-ttu-id="18837-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18837-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="18837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18837-102">SYNOPSIS</span></span>
<span data-ttu-id="18837-103">저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-103">Lists storage queues.</span></span>

## <span data-ttu-id="18837-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18837-104">SYNTAX</span></span>

### <span data-ttu-id="18837-105">QueueName (기본값)</span><span class="sxs-lookup"><span data-stu-id="18837-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="18837-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="18837-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="18837-107">설명은</span><span class="sxs-lookup"><span data-stu-id="18837-107">DESCRIPTION</span></span>
<span data-ttu-id="18837-108">**AzureStorageQueue** Cmdlet은 Azure 저장소 계정과 연결 된 저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="18837-109">예제의</span><span class="sxs-lookup"><span data-stu-id="18837-109">EXAMPLES</span></span>

### <span data-ttu-id="18837-110">예제 1: 모든 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="18837-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="18837-111">이 명령은 현재 저장소 계정에 대 한 모든 저장소 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18837-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="18837-112">예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="18837-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="18837-113">이 명령은 와일드 카드 문자를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18837-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="18837-114">예제 3: 큐 이름 접두사를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="18837-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="18837-115">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18837-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="18837-116">변수</span><span class="sxs-lookup"><span data-stu-id="18837-116">PARAMETERS</span></span>

### <span data-ttu-id="18837-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="18837-117">-Context</span></span>
<span data-ttu-id="18837-118">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="18837-119">**새로운-AzureStorageContext** cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18837-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="18837-120">-이름</span><span class="sxs-lookup"><span data-stu-id="18837-120">-Name</span></span>
<span data-ttu-id="18837-121">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-121">Specifies a name.</span></span>
<span data-ttu-id="18837-122">이름을 지정 하지 않으면 cmdlet에서 모든 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18837-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="18837-123">전체 또는 일부 이름을 지정한 경우 cmdlet은 이름 패턴과 일치 하는 모든 큐를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18837-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18837-124">-접두사</span><span class="sxs-lookup"><span data-stu-id="18837-124">-Prefix</span></span>
<span data-ttu-id="18837-125">가져오려는 큐 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18837-126">CommonParameters</span></span>
<span data-ttu-id="18837-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18837-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18837-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18837-129">입력</span><span class="sxs-lookup"><span data-stu-id="18837-129">INPUTS</span></span>

## <span data-ttu-id="18837-130">출력</span><span class="sxs-lookup"><span data-stu-id="18837-130">OUTPUTS</span></span>

## <span data-ttu-id="18837-131">상속자</span><span class="sxs-lookup"><span data-stu-id="18837-131">NOTES</span></span>

## <span data-ttu-id="18837-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18837-132">RELATED LINKS</span></span>

[<span data-ttu-id="18837-133">새로운 AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18837-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="18837-134">제거-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18837-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


