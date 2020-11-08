---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045937"
---
# <span data-ttu-id="9db08-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="9db08-101">Test-AzureName</span></span>

## <span data-ttu-id="9db08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9db08-102">SYNOPSIS</span></span>
<span data-ttu-id="9db08-103">Microsoft Azure 클라우드 서비스 이름, 저장소 서비스 이름 또는 서비스 버스 네임 스페이스 이름이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="9db08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9db08-104">SYNTAX</span></span>

### <span data-ttu-id="9db08-105">Services</span><span class="sxs-lookup"><span data-stu-id="9db08-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9db08-106">용량</span><span class="sxs-lookup"><span data-stu-id="9db08-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9db08-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9db08-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9db08-108">웹 사이트</span><span class="sxs-lookup"><span data-stu-id="9db08-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9db08-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9db08-109">DESCRIPTION</span></span>
<span data-ttu-id="9db08-110">이름이 있으면 cmdlet이 $True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="9db08-111">이름이 없는 경우 $False 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="9db08-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9db08-112">EXAMPLES</span></span>

### <span data-ttu-id="9db08-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9db08-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="9db08-114">이 명령을 테스트 하 여 "MyNameService1"이 기존 Microsoft Azure 클라우드 서비스 이름 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="9db08-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9db08-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="9db08-116">이 명령은 "mystorename1"이 기존 Microsoft Azure 저장소 서비스 이름 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="9db08-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="9db08-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="9db08-118">이 명령을 테스트 하 여 "mynamespace"이 기존 Microsoft Azure service bus 네임 스페이스 이름 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="9db08-119">변수</span><span class="sxs-lookup"><span data-stu-id="9db08-119">PARAMETERS</span></span>

### <span data-ttu-id="9db08-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9db08-120">-Name</span></span>
<span data-ttu-id="9db08-121">테스트할 서비스 또는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-121">Specifies the name of the service or storage account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db08-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="9db08-122">-Profile</span></span>
<span data-ttu-id="9db08-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9db08-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9db08-125">-서비스</span><span class="sxs-lookup"><span data-stu-id="9db08-125">-Service</span></span>
<span data-ttu-id="9db08-126">기존 서비스 계정을 테스트 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db08-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9db08-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="9db08-128">기존 service bus 네임 스페이스를 테스트 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db08-129">-저장소</span><span class="sxs-lookup"><span data-stu-id="9db08-129">-Storage</span></span>
<span data-ttu-id="9db08-130">기존 저장소 계정을 테스트 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db08-131">-웹 사이트</span><span class="sxs-lookup"><span data-stu-id="9db08-131">-Website</span></span>
<span data-ttu-id="9db08-132">기존 웹 사이트를 테스트 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db08-133">CommonParameters</span></span>
<span data-ttu-id="9db08-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db08-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db08-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db08-136">입력</span><span class="sxs-lookup"><span data-stu-id="9db08-136">INPUTS</span></span>

## <span data-ttu-id="9db08-137">출력</span><span class="sxs-lookup"><span data-stu-id="9db08-137">OUTPUTS</span></span>

## <span data-ttu-id="9db08-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9db08-138">NOTES</span></span>
* <span data-ttu-id="9db08-139">노드 개발자, php-개발자, python-개발자</span><span class="sxs-lookup"><span data-stu-id="9db08-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="9db08-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9db08-140">RELATED LINKS</span></span>

