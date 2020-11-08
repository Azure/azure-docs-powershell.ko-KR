---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046049"
---
# <span data-ttu-id="8a148-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="8a148-101">Set-AzureService</span></span>

## <span data-ttu-id="8a148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a148-102">SYNOPSIS</span></span>
<span data-ttu-id="8a148-103">지정 된 Microsoft Azure 서비스의 레이블 및 설명을 설정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="8a148-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a148-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a148-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a148-105">DESCRIPTION</span></span>
<span data-ttu-id="8a148-106">**집합-azureservice** cmdlet은 현재 구독의 서비스에 대 한 레이블 및 설명을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="8a148-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a148-107">EXAMPLES</span></span>

### <span data-ttu-id="8a148-108">예제 1: 서비스의 레이블 및 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="8a148-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="8a148-109">이 명령은 "MyTestSvc1" 라는 레이블을 설정 하 고 MyTestSvc1 서비스에 대 한 "새 구성을 테스트 하기 위해 내 서비스"에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="8a148-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a148-110">PARAMETERS</span></span>

### <span data-ttu-id="8a148-111">-설명</span><span class="sxs-lookup"><span data-stu-id="8a148-111">-Description</span></span>
<span data-ttu-id="8a148-112">Azure 서비스에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="8a148-113">설명은 최대 1024 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a148-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a148-114">-InformationAction</span></span>
<span data-ttu-id="8a148-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a148-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a148-117">하기로</span><span class="sxs-lookup"><span data-stu-id="8a148-117">Continue</span></span>
- <span data-ttu-id="8a148-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="8a148-118">Ignore</span></span>
- <span data-ttu-id="8a148-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="8a148-119">Inquire</span></span>
- <span data-ttu-id="8a148-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a148-120">SilentlyContinue</span></span>
- <span data-ttu-id="8a148-121">중지가</span><span class="sxs-lookup"><span data-stu-id="8a148-121">Stop</span></span>
- <span data-ttu-id="8a148-122">대기</span><span class="sxs-lookup"><span data-stu-id="8a148-122">Suspend</span></span>

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

### <span data-ttu-id="8a148-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a148-123">-InformationVariable</span></span>
<span data-ttu-id="8a148-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a148-125">-레이블</span><span class="sxs-lookup"><span data-stu-id="8a148-125">-Label</span></span>
<span data-ttu-id="8a148-126">Azure 서비스의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="8a148-127">레이블은 최대 100 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a148-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="8a148-128">-Profile</span></span>
<span data-ttu-id="8a148-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a148-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a148-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="8a148-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="8a148-132">역방향 DNS에 대해 정규화 된 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a148-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8a148-133">-ServiceName</span></span>
<span data-ttu-id="8a148-134">업데이트할 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-134">Specifies the name of the Azure service to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a148-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a148-135">CommonParameters</span></span>
<span data-ttu-id="8a148-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a148-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a148-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a148-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a148-138">입력</span><span class="sxs-lookup"><span data-stu-id="8a148-138">INPUTS</span></span>

## <span data-ttu-id="8a148-139">출력</span><span class="sxs-lookup"><span data-stu-id="8a148-139">OUTPUTS</span></span>

### <span data-ttu-id="8a148-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8a148-140">ManagementOperationContext</span></span>

## <span data-ttu-id="8a148-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8a148-141">NOTES</span></span>

## <span data-ttu-id="8a148-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a148-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a148-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="8a148-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="8a148-144">새-AzureService</span><span class="sxs-lookup"><span data-stu-id="8a148-144">New-AzureService</span></span>](./New-AzureService.md)


