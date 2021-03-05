---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002416"
---
# <span data-ttu-id="85f55-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85f55-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="85f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f55-102">SYNOPSIS</span></span>
<span data-ttu-id="85f55-103">저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-103">Creates a storage queue.</span></span>

## <span data-ttu-id="85f55-104">구문</span><span class="sxs-lookup"><span data-stu-id="85f55-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85f55-105">설명</span><span class="sxs-lookup"><span data-stu-id="85f55-105">DESCRIPTION</span></span>
<span data-ttu-id="85f55-106">**New-AzStorageQueue** cmdlet은 Azure에서 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="85f55-107">예제</span><span class="sxs-lookup"><span data-stu-id="85f55-107">EXAMPLES</span></span>

### <span data-ttu-id="85f55-108">예제 1: Azure 저장소 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="85f55-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="85f55-109">이 예제에서는 queueabc라는 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="85f55-110">예제 2: 여러 Azure Storage 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="85f55-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="85f55-111">이 예제에서는 여러 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="85f55-112">.NET String 클래스의 분할 메서드를 사용하여 파이프라인의 이름을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="85f55-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85f55-113">PARAMETERS</span></span>

### <span data-ttu-id="85f55-114">-Context</span><span class="sxs-lookup"><span data-stu-id="85f55-114">-Context</span></span>
<span data-ttu-id="85f55-115">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="85f55-116">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="85f55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f55-117">-DefaultProfile</span></span>
<span data-ttu-id="85f55-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f55-119">-Name</span><span class="sxs-lookup"><span data-stu-id="85f55-119">-Name</span></span>
<span data-ttu-id="85f55-120">큐의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85f55-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f55-121">CommonParameters</span></span>
<span data-ttu-id="85f55-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85f55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f55-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="85f55-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f55-124">입력</span><span class="sxs-lookup"><span data-stu-id="85f55-124">INPUTS</span></span>

### <span data-ttu-id="85f55-125">System.String</span><span class="sxs-lookup"><span data-stu-id="85f55-125">System.String</span></span>

### <span data-ttu-id="85f55-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="85f55-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="85f55-127">출력</span><span class="sxs-lookup"><span data-stu-id="85f55-127">OUTPUTS</span></span>

### <span data-ttu-id="85f55-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85f55-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="85f55-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85f55-129">NOTES</span></span>

## <span data-ttu-id="85f55-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85f55-130">RELATED LINKS</span></span>

[<span data-ttu-id="85f55-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85f55-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="85f55-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="85f55-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


