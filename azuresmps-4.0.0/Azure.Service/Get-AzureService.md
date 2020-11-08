---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046309"
---
# <span data-ttu-id="1f302-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="1f302-101">Get-AzureService</span></span>

## <span data-ttu-id="1f302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f302-102">SYNOPSIS</span></span>
<span data-ttu-id="1f302-103">현재 구독에 대 한 클라우드 서비스에 대 한 정보가 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="1f302-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f302-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1f302-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f302-105">DESCRIPTION</span></span>
<span data-ttu-id="1f302-106">**Get-AzureService** cmdlet은 현재 구독과 연결 된 모든 Azure 클라우드 서비스가 포함 된 list 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="1f302-107">*ServiceName* 매개 변수를 지정 하면 **Get-azureservice** 는 일치 하는 서비스에 대 한 정보만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="1f302-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1f302-108">EXAMPLES</span></span>

### <span data-ttu-id="1f302-109">예제 1: 모든 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f302-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="1f302-110">이 명령은 현재 구독과 연결 된 모든 Azure 서비스에 대 한 정보를 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="1f302-111">예제 2: 지정 된 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f302-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="1f302-112">이 명령은 $MySvc 서비스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="1f302-113">예제 3: 사용 가능한 메서드 및 속성 표시</span><span class="sxs-lookup"><span data-stu-id="1f302-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="1f302-114">이 명령은 **가져오기-AzureService** cmdlet에서 사용할 수 있는 속성 및 메서드를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="1f302-115">변수</span><span class="sxs-lookup"><span data-stu-id="1f302-115">PARAMETERS</span></span>

### <span data-ttu-id="1f302-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1f302-116">-InformationAction</span></span>
<span data-ttu-id="1f302-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1f302-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f302-119">하기로</span><span class="sxs-lookup"><span data-stu-id="1f302-119">Continue</span></span>
- <span data-ttu-id="1f302-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="1f302-120">Ignore</span></span>
- <span data-ttu-id="1f302-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="1f302-121">Inquire</span></span>
- <span data-ttu-id="1f302-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1f302-122">SilentlyContinue</span></span>
- <span data-ttu-id="1f302-123">중지가</span><span class="sxs-lookup"><span data-stu-id="1f302-123">Stop</span></span>
- <span data-ttu-id="1f302-124">대기</span><span class="sxs-lookup"><span data-stu-id="1f302-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f302-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1f302-125">-InformationVariable</span></span>
<span data-ttu-id="1f302-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f302-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="1f302-127">-Profile</span></span>
<span data-ttu-id="1f302-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f302-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f302-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1f302-130">-ServiceName</span></span>
<span data-ttu-id="1f302-131">정보를 반환할 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f302-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f302-132">CommonParameters</span></span>
<span data-ttu-id="1f302-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f302-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f302-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f302-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f302-135">입력</span><span class="sxs-lookup"><span data-stu-id="1f302-135">INPUTS</span></span>

## <span data-ttu-id="1f302-136">출력</span><span class="sxs-lookup"><span data-stu-id="1f302-136">OUTPUTS</span></span>

### <span data-ttu-id="1f302-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="1f302-137">HostedServiceContext</span></span>

## <span data-ttu-id="1f302-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1f302-138">NOTES</span></span>

## <span data-ttu-id="1f302-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f302-139">RELATED LINKS</span></span>

[<span data-ttu-id="1f302-140">새-AzureService</span><span class="sxs-lookup"><span data-stu-id="1f302-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="1f302-141">Set AzureService</span><span class="sxs-lookup"><span data-stu-id="1f302-141">Set-AzureService</span></span>](./Set-AzureService.md)


