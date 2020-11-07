---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 1f0e9f17ea6d240f9f29f677325173e0bbef38f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698653"
---
# <span data-ttu-id="545ad-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="545ad-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="545ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545ad-102">SYNOPSIS</span></span>
<span data-ttu-id="545ad-103">저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-103">Lists storage queues.</span></span>

## <span data-ttu-id="545ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="545ad-104">SYNTAX</span></span>

### <span data-ttu-id="545ad-105">QueueName (기본값)</span><span class="sxs-lookup"><span data-stu-id="545ad-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="545ad-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="545ad-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="545ad-107">설명은</span><span class="sxs-lookup"><span data-stu-id="545ad-107">DESCRIPTION</span></span>
<span data-ttu-id="545ad-108">**AzStorageQueue** Cmdlet은 Azure 저장소 계정과 연결 된 저장소 큐를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="545ad-109">예제의</span><span class="sxs-lookup"><span data-stu-id="545ad-109">EXAMPLES</span></span>

### <span data-ttu-id="545ad-110">예제 1: 모든 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="545ad-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="545ad-111">이 명령은 현재 저장소 계정에 대 한 모든 저장소 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="545ad-112">예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="545ad-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="545ad-113">이 명령은 와일드 카드 문자를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="545ad-114">예제 3: 큐 이름 접두사를 사용 하 여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="545ad-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="545ad-115">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="545ad-116">변수</span><span class="sxs-lookup"><span data-stu-id="545ad-116">PARAMETERS</span></span>

### <span data-ttu-id="545ad-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="545ad-117">-Context</span></span>
<span data-ttu-id="545ad-118">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="545ad-119">**새 AzStorageContext** cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="545ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545ad-120">-DefaultProfile</span></span>
<span data-ttu-id="545ad-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545ad-122">-이름</span><span class="sxs-lookup"><span data-stu-id="545ad-122">-Name</span></span>
<span data-ttu-id="545ad-123">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-123">Specifies a name.</span></span>
<span data-ttu-id="545ad-124">이름을 지정 하지 않으면 cmdlet에서 모든 큐의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="545ad-125">전체 또는 일부 이름을 지정한 경우 cmdlet은 이름 패턴과 일치 하는 모든 큐를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="545ad-126">-접두사</span><span class="sxs-lookup"><span data-stu-id="545ad-126">-Prefix</span></span>
<span data-ttu-id="545ad-127">가져오려는 큐 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="545ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545ad-128">CommonParameters</span></span>
<span data-ttu-id="545ad-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545ad-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545ad-131">입력</span><span class="sxs-lookup"><span data-stu-id="545ad-131">INPUTS</span></span>

### <span data-ttu-id="545ad-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="545ad-132">System.String</span></span>

### <span data-ttu-id="545ad-133">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="545ad-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="545ad-134">출력</span><span class="sxs-lookup"><span data-stu-id="545ad-134">OUTPUTS</span></span>

### <span data-ttu-id="545ad-135">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="545ad-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="545ad-136">상속자</span><span class="sxs-lookup"><span data-stu-id="545ad-136">NOTES</span></span>

## <span data-ttu-id="545ad-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="545ad-137">RELATED LINKS</span></span>

[<span data-ttu-id="545ad-138">새로운 AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="545ad-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="545ad-139">제거-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="545ad-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


