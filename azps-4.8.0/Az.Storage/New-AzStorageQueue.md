---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056887"
---
# <span data-ttu-id="8d9a9-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8d9a9-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="8d9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9a9-103">저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-103">Creates a storage queue.</span></span>

## <span data-ttu-id="8d9a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d9a9-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9a9-106">**AzStorageQueue** Cmdlet은 Azure에서 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="8d9a9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9a9-108">예제 1: Azure 저장소 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="8d9a9-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="8d9a9-109">이 예제에서는 queueabc 라는 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="8d9a9-110">예제 2: 여러 azure storage 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="8d9a9-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="8d9a9-111">이 예제에서는 여러 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="8d9a9-112">.NET 문자열 클래스의 Split 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="8d9a9-113">변수</span><span class="sxs-lookup"><span data-stu-id="8d9a9-113">PARAMETERS</span></span>

### <span data-ttu-id="8d9a9-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8d9a9-114">-Context</span></span>
<span data-ttu-id="8d9a9-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8d9a9-116">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8d9a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9a9-117">-DefaultProfile</span></span>
<span data-ttu-id="8d9a9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9a9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8d9a9-119">-Name</span></span>
<span data-ttu-id="8d9a9-120">큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="8d9a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9a9-121">CommonParameters</span></span>
<span data-ttu-id="8d9a9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9a9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9a9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9a9-124">입력</span><span class="sxs-lookup"><span data-stu-id="8d9a9-124">INPUTS</span></span>

### <span data-ttu-id="8d9a9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d9a9-125">System.String</span></span>

### <span data-ttu-id="8d9a9-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d9a9-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d9a9-127">출력</span><span class="sxs-lookup"><span data-stu-id="8d9a9-127">OUTPUTS</span></span>

### <span data-ttu-id="8d9a9-128">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a9-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="8d9a9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8d9a9-129">NOTES</span></span>

## <span data-ttu-id="8d9a9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d9a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="8d9a9-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8d9a9-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="8d9a9-132">제거-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8d9a9-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


