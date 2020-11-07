---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1ce3615d7eeef4986f1fefd20ec5be2ea1aaac7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876258"
---
# <span data-ttu-id="cb5e7-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cb5e7-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="cb5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5e7-103">저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-103">Creates a storage queue.</span></span>

## <span data-ttu-id="cb5e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb5e7-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb5e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5e7-106">**AzStorageQueue** Cmdlet은 Azure에서 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="cb5e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cb5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="cb5e7-108">예제 1: Azure 저장소 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="cb5e7-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="cb5e7-109">이 예제에서는 queueabc 라는 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="cb5e7-110">예제 2: 여러 azure storage 큐 만들기</span><span class="sxs-lookup"><span data-stu-id="cb5e7-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="cb5e7-111">이 예제에서는 여러 저장소 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="cb5e7-112">.NET 문자열 클래스의 Split 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="cb5e7-113">변수</span><span class="sxs-lookup"><span data-stu-id="cb5e7-113">PARAMETERS</span></span>

### <span data-ttu-id="cb5e7-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cb5e7-114">-Context</span></span>
<span data-ttu-id="cb5e7-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cb5e7-116">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cb5e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5e7-117">-DefaultProfile</span></span>
<span data-ttu-id="cb5e7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb5e7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cb5e7-119">-Name</span></span>
<span data-ttu-id="cb5e7-120">큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="cb5e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5e7-121">CommonParameters</span></span>
<span data-ttu-id="cb5e7-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5e7-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5e7-124">입력</span><span class="sxs-lookup"><span data-stu-id="cb5e7-124">INPUTS</span></span>

### <span data-ttu-id="cb5e7-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb5e7-125">System.String</span></span>

### <span data-ttu-id="cb5e7-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb5e7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cb5e7-127">출력</span><span class="sxs-lookup"><span data-stu-id="cb5e7-127">OUTPUTS</span></span>

### <span data-ttu-id="cb5e7-128">WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="cb5e7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="cb5e7-129">NOTES</span></span>

## <span data-ttu-id="cb5e7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb5e7-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb5e7-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cb5e7-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="cb5e7-132">제거-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cb5e7-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


