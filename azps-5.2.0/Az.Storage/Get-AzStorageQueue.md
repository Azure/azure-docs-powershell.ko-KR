---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324953"
---
# <span data-ttu-id="133ee-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="133ee-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="133ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="133ee-102">SYNOPSIS</span></span>
<span data-ttu-id="133ee-103">저장소 큐를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-103">Lists storage queues.</span></span>

## <span data-ttu-id="133ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="133ee-104">SYNTAX</span></span>

### <span data-ttu-id="133ee-105">QueueName(기본값)</span><span class="sxs-lookup"><span data-stu-id="133ee-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="133ee-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="133ee-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="133ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="133ee-107">DESCRIPTION</span></span>
<span data-ttu-id="133ee-108">**Get-AzStorageQueue** cmdlet은 Azure Storage 계정과 연결된 스토리지 큐를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="133ee-109">예제</span><span class="sxs-lookup"><span data-stu-id="133ee-109">EXAMPLES</span></span>

### <span data-ttu-id="133ee-110">예제 1: 모든 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="133ee-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="133ee-111">이 명령은 현재 Storage 계정에 대한 모든 저장소 큐 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="133ee-112">예제 2: 와일드카드 문자를 사용하여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="133ee-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="133ee-113">이 명령은 와일드카드 문자를 사용하여 이름이 큐로 시작하는 저장소 큐 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="133ee-114">예제 3: 큐 이름 사전을 사용하여 Azure Storage 큐 나열</span><span class="sxs-lookup"><span data-stu-id="133ee-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="133ee-115">이 예제에서는 *Prefix* 매개 변수를 사용하여 이름이 큐로 시작하는 저장소 큐 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="133ee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="133ee-116">PARAMETERS</span></span>

### <span data-ttu-id="133ee-117">-Context</span><span class="sxs-lookup"><span data-stu-id="133ee-117">-Context</span></span>
<span data-ttu-id="133ee-118">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="133ee-119">**New-AzStorageContext** cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="133ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133ee-120">-DefaultProfile</span></span>
<span data-ttu-id="133ee-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="133ee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="133ee-122">-Name</span></span>
<span data-ttu-id="133ee-123">이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-123">Specifies a name.</span></span>
<span data-ttu-id="133ee-124">이름을 지정하지 않으면 cmdlet은 모든 큐의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="133ee-125">전체 또는 부분 이름을 지정하면 cmdlet은 이름 패턴과 일치하는 모든 큐를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="133ee-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="133ee-126">-Prefix</span></span>
<span data-ttu-id="133ee-127">얻게 할 큐 이름에 사용되는 prefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="133ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133ee-128">CommonParameters</span></span>
<span data-ttu-id="133ee-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="133ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133ee-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="133ee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133ee-131">입력</span><span class="sxs-lookup"><span data-stu-id="133ee-131">INPUTS</span></span>

### <span data-ttu-id="133ee-132">System.String</span><span class="sxs-lookup"><span data-stu-id="133ee-132">System.String</span></span>

### <span data-ttu-id="133ee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="133ee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="133ee-134">출력</span><span class="sxs-lookup"><span data-stu-id="133ee-134">OUTPUTS</span></span>

### <span data-ttu-id="133ee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="133ee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="133ee-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="133ee-136">NOTES</span></span>

## <span data-ttu-id="133ee-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="133ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="133ee-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="133ee-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="133ee-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="133ee-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)

