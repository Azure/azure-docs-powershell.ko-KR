---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046508"
---
# <span data-ttu-id="0a1e0-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="0a1e0-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="0a1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1e0-103">클라우드 VM 역할 크기 프로필 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="0a1e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a1e0-104">SYNTAX</span></span>

### <span data-ttu-id="0a1e0-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a1e0-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a1e0-106">FromName</span><span class="sxs-lookup"><span data-stu-id="0a1e0-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a1e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0a1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="0a1e0-108">**WAPackCloudVMRoleSizeProfile** cmdlet은 가상 컴퓨터에 대 한 클라우드 VM 역할 크기 프로필 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="0a1e0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="0a1e0-110">예제 1: 이름을 사용 하 여 클라우드 VM 역할 크기 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a1e0-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="0a1e0-111">이 명령은 Small 이라는 크기 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="0a1e0-112">예제 2: 모든 클라우드 VM 역할 크기 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a1e0-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="0a1e0-113">이 명령은 모든 크기 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="0a1e0-114">변수</span><span class="sxs-lookup"><span data-stu-id="0a1e0-114">PARAMETERS</span></span>

### <span data-ttu-id="0a1e0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0a1e0-115">-Name</span></span>
<span data-ttu-id="0a1e0-116">클라우드 VM 역할 크기 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a1e0-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="0a1e0-117">-Profile</span></span>
<span data-ttu-id="0a1e0-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a1e0-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a1e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1e0-120">CommonParameters</span></span>
<span data-ttu-id="0a1e0-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a1e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1e0-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1e0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1e0-123">입력</span><span class="sxs-lookup"><span data-stu-id="0a1e0-123">INPUTS</span></span>

## <span data-ttu-id="0a1e0-124">출력</span><span class="sxs-lookup"><span data-stu-id="0a1e0-124">OUTPUTS</span></span>

## <span data-ttu-id="0a1e0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="0a1e0-125">NOTES</span></span>

## <span data-ttu-id="0a1e0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a1e0-126">RELATED LINKS</span></span>

[<span data-ttu-id="0a1e0-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0a1e0-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


