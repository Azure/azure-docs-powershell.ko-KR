---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045630"
---
# <span data-ttu-id="cd6e5-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="cd6e5-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="cd6e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6e5-103">더 이상 존재 하지 않는 Azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="cd6e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd6e5-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd6e5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6e5-106">**AzureRemoteAppVmStaleAdObject** cmdlet은 더 이상 존재 하지 않는 azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="cd6e5-107">이 cmdlet은 가져오는 각 개체의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="cd6e5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cd6e5-108">EXAMPLES</span></span>

### <span data-ttu-id="cd6e5-109">예제 1: 컬렉션에 대 한 부실 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd6e5-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="cd6e5-110">이 두 번째 명령은 Contoso 라는 컬렉션에 대 한 부실 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="cd6e5-111">변수</span><span class="sxs-lookup"><span data-stu-id="cd6e5-111">PARAMETERS</span></span>

### <span data-ttu-id="cd6e5-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="cd6e5-112">-CollectionName</span></span>
<span data-ttu-id="cd6e5-113">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e5-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="cd6e5-114">-Credential</span></span>
<span data-ttu-id="cd6e5-115">이 작업을 수행할 수 있는 권한이 있는 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="cd6e5-116">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="cd6e5-117">이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 사용자 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e5-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="cd6e5-118">-Profile</span></span>
<span data-ttu-id="cd6e5-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd6e5-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd6e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6e5-121">CommonParameters</span></span>
<span data-ttu-id="cd6e5-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6e5-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6e5-124">입력</span><span class="sxs-lookup"><span data-stu-id="cd6e5-124">INPUTS</span></span>

## <span data-ttu-id="cd6e5-125">출력</span><span class="sxs-lookup"><span data-stu-id="cd6e5-125">OUTPUTS</span></span>

### <span data-ttu-id="cd6e5-126">이름</span><span class="sxs-lookup"><span data-stu-id="cd6e5-126">String</span></span>

## <span data-ttu-id="cd6e5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="cd6e5-127">NOTES</span></span>

## <span data-ttu-id="cd6e5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd6e5-128">RELATED LINKS</span></span>

[<span data-ttu-id="cd6e5-129">일반-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="cd6e5-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


