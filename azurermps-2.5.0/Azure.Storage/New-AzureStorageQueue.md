---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882050"
---
# <span data-ttu-id="f27be-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f27be-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="f27be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27be-102">SYNOPSIS</span></span>
<span data-ttu-id="f27be-103">저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f27be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f27be-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f27be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f27be-105">DESCRIPTION</span></span>
<span data-ttu-id="f27be-106">**AzureStorageQueue** Cmdlet은 Azure에서 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="f27be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f27be-107">EXAMPLES</span></span>

### <span data-ttu-id="f27be-108">예제 1: Azure 저장소 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="f27be-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="f27be-109">이 예제에서는 queueabc 라는 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="f27be-110">예제 2: 여러 azure storage 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="f27be-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="f27be-111">이 예제에서는 여러 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="f27be-112">.NET 문자열 클래스의 Split 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="f27be-113">변수</span><span class="sxs-lookup"><span data-stu-id="f27be-113">PARAMETERS</span></span>

### <span data-ttu-id="f27be-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f27be-114">-Context</span></span>
<span data-ttu-id="f27be-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f27be-116">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f27be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27be-117">-DefaultProfile</span></span>
<span data-ttu-id="f27be-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27be-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f27be-119">-Name</span></span>
<span data-ttu-id="f27be-120">큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="f27be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27be-121">CommonParameters</span></span>
<span data-ttu-id="f27be-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27be-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27be-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27be-124">입력</span><span class="sxs-lookup"><span data-stu-id="f27be-124">INPUTS</span></span>

### <span data-ttu-id="f27be-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f27be-125">System.String</span></span>

### <span data-ttu-id="f27be-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f27be-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f27be-127">출력</span><span class="sxs-lookup"><span data-stu-id="f27be-127">OUTPUTS</span></span>

### <span data-ttu-id="f27be-128">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27be-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="f27be-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f27be-129">NOTES</span></span>

## <span data-ttu-id="f27be-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f27be-130">RELATED LINKS</span></span>

[<span data-ttu-id="f27be-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f27be-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="f27be-132">제거-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f27be-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)

