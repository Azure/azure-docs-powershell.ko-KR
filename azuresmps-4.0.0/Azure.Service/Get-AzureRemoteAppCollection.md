---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046329"
---
# <span data-ttu-id="9b062-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9b062-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="9b062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b062-102">SYNOPSIS</span></span>
<span data-ttu-id="9b062-103">Azure RemoteApp 컬렉션에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9b062-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b062-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9b062-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b062-105">DESCRIPTION</span></span>
<span data-ttu-id="9b062-106">**AzureRemoteAppCollection** Cmdlet은 Microsoft Azure의 Azure RemoteApp 컬렉션에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="9b062-107">이 메서드는 특정 컬렉션에 대 한 정보를 포함 하는 개체를 반환 하 고, 지정 된 컬렉션이 없는 경우에는 현재 구독의 모든 컬렉션에 대해 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="9b062-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9b062-108">EXAMPLES</span></span>

### <span data-ttu-id="9b062-109">예제 1: 모든 컬렉션 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b062-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="9b062-110">이 명령은 구독에 있는 모든 Azure RemoteApp 컬렉션 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="9b062-111">예제 2: 지정 된 컬렉션에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b062-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="9b062-112">이 명령은 ContosoApps 이라는 Azure RemoteApp 컬렉션에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="9b062-113">예제 3: 와일드 카드를 사용 하 여 컬렉션 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b062-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="9b062-114">이 명령은 모든 Azure RemoteApp 컬렉션 일치 재무 \*의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="9b062-115">변수</span><span class="sxs-lookup"><span data-stu-id="9b062-115">PARAMETERS</span></span>

### <span data-ttu-id="9b062-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9b062-116">-CollectionName</span></span>
<span data-ttu-id="9b062-117">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9b062-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="9b062-118">-Profile</span></span>
<span data-ttu-id="9b062-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b062-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b062-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b062-121">CommonParameters</span></span>
<span data-ttu-id="9b062-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b062-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b062-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b062-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b062-124">입력</span><span class="sxs-lookup"><span data-stu-id="9b062-124">INPUTS</span></span>

## <span data-ttu-id="9b062-125">출력</span><span class="sxs-lookup"><span data-stu-id="9b062-125">OUTPUTS</span></span>

## <span data-ttu-id="9b062-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9b062-126">NOTES</span></span>

## <span data-ttu-id="9b062-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b062-127">RELATED LINKS</span></span>

[<span data-ttu-id="9b062-128">새로운 AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9b062-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="9b062-129">제거-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9b062-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="9b062-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9b062-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="9b062-131">업데이트-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9b062-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


