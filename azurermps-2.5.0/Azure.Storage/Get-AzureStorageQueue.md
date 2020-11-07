---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883233"
---
# <span data-ttu-id="f810a-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f810a-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="f810a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f810a-102">SYNOPSIS</span></span>
<span data-ttu-id="f810a-103">저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f810a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f810a-104">SYNTAX</span></span>

### <span data-ttu-id="f810a-105">QueueName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f810a-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f810a-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="f810a-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f810a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f810a-107">DESCRIPTION</span></span>
<span data-ttu-id="f810a-108">**AzureStorageQueue** Cmdlet은 Azure 저장소 계정과 연결 된 저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="f810a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f810a-109">EXAMPLES</span></span>

### <span data-ttu-id="f810a-110">예제 1: 모든 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="f810a-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="f810a-111">이 명령은 현재 저장소 계정에 대 한 모든 저장소 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="f810a-112">예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="f810a-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="f810a-113">이 명령은 와일드 카드 문자를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="f810a-114">예제 3: 큐 이름 접두사를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="f810a-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="f810a-115">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="f810a-116">변수</span><span class="sxs-lookup"><span data-stu-id="f810a-116">PARAMETERS</span></span>

### <span data-ttu-id="f810a-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f810a-117">-Context</span></span>
<span data-ttu-id="f810a-118">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f810a-119">**새로운-AzureStorageContext** cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f810a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f810a-120">-DefaultProfile</span></span>
<span data-ttu-id="f810a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f810a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f810a-122">-Name</span></span>
<span data-ttu-id="f810a-123">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-123">Specifies a name.</span></span>
<span data-ttu-id="f810a-124">이름을 지정 하지 않으면 cmdlet에서 모든 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="f810a-125">전체 또는 일부 이름을 지정한 경우 cmdlet은 이름 패턴과 일치 하는 모든 큐를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f810a-126">-접두사</span><span class="sxs-lookup"><span data-stu-id="f810a-126">-Prefix</span></span>
<span data-ttu-id="f810a-127">가져오려는 큐 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f810a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f810a-128">CommonParameters</span></span>
<span data-ttu-id="f810a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f810a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f810a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f810a-131">입력</span><span class="sxs-lookup"><span data-stu-id="f810a-131">INPUTS</span></span>

### <span data-ttu-id="f810a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f810a-132">System.String</span></span>

### <span data-ttu-id="f810a-133">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f810a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f810a-134">출력</span><span class="sxs-lookup"><span data-stu-id="f810a-134">OUTPUTS</span></span>

### <span data-ttu-id="f810a-135">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f810a-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="f810a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f810a-136">NOTES</span></span>

## <span data-ttu-id="f810a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f810a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f810a-138">새로운 AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f810a-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="f810a-139">제거-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f810a-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


