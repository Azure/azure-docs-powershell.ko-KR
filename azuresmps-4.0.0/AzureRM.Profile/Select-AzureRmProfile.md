---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523556"
---
# <span data-ttu-id="9fe24-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="9fe24-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="9fe24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe24-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe24-103">파일에서 Azure 인증 정보를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="9fe24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fe24-104">SYNTAX</span></span>

### <span data-ttu-id="9fe24-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="9fe24-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="9fe24-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="9fe24-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="9fe24-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9fe24-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe24-108">Select-AzureRmProfile cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="9fe24-109">현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="9fe24-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9fe24-110">EXAMPLES</span></span>

### <span data-ttu-id="9fe24-111">예제 1: PSAzureProfile에서 프로필 선택</span><span class="sxs-lookup"><span data-stu-id="9fe24-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="9fe24-112">이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile의 프로필을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="9fe24-113">예제 2: JSON 파일에서 프로필 선택</span><span class="sxs-lookup"><span data-stu-id="9fe24-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="9fe24-114">이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 프로필을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="9fe24-115">이 JSON 파일은 Save-AzureRmProfile에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="9fe24-116">변수</span><span class="sxs-lookup"><span data-stu-id="9fe24-116">PARAMETERS</span></span>

### <span data-ttu-id="9fe24-117">-Path</span><span class="sxs-lookup"><span data-stu-id="9fe24-117">-Path</span></span>
<span data-ttu-id="9fe24-118">저장-AzureRMProfile를 사용 하 여 저장 된 프로필 정보의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe24-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="9fe24-119">-Profile</span></span>
<span data-ttu-id="9fe24-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9fe24-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe24-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe24-122">CommonParameters</span></span>
<span data-ttu-id="9fe24-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe24-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe24-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe24-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe24-125">입력</span><span class="sxs-lookup"><span data-stu-id="9fe24-125">INPUTS</span></span>

## <span data-ttu-id="9fe24-126">출력</span><span class="sxs-lookup"><span data-stu-id="9fe24-126">OUTPUTS</span></span>

### <span data-ttu-id="9fe24-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="9fe24-127">PSAzureProfile</span></span>

## <span data-ttu-id="9fe24-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9fe24-128">NOTES</span></span>

## <span data-ttu-id="9fe24-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fe24-129">RELATED LINKS</span></span>

[<span data-ttu-id="9fe24-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="9fe24-130">Get-AzureRMContext</span></span>]()

