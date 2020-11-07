---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
ms.openlocfilehash: 0f452818db1af3f3a69db58f82b89e6cfa8ee461
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880518"
---
# <span data-ttu-id="6387b-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="6387b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6387b-102">SYNOPSIS</span></span>
<span data-ttu-id="6387b-103">새 작업 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6387b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6387b-104">SYNTAX</span></span>

### <span data-ttu-id="6387b-105">NewEmailReceiver (기본값)</span><span class="sxs-lookup"><span data-stu-id="6387b-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6387b-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6387b-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6387b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6387b-108">DESCRIPTION</span></span>
<span data-ttu-id="6387b-109">**새 AzureRmActionGroupReceiver** cmdlet은 메모리에 새 동작 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="6387b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6387b-110">EXAMPLES</span></span>

### <span data-ttu-id="6387b-111">예제 1: 메모리에서 새 전자 메일 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="6387b-112">이 명령은 메모리에 새 전자 메일 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="6387b-113">예제 2: 메모리에 새 SMS 받는 사람 만들기</span><span class="sxs-lookup"><span data-stu-id="6387b-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="6387b-114">이 명령은 메모리에 새 SMS 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="6387b-115">예제 3: 메모리에 새 webhook 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="6387b-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="6387b-116">이 명령은 메모리에 새 webhook 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="6387b-117">변수</span><span class="sxs-lookup"><span data-stu-id="6387b-117">PARAMETERS</span></span>

### <span data-ttu-id="6387b-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6387b-118">-CountryCode</span></span>
<span data-ttu-id="6387b-119">SMS 받는 사람에 대 한 국가 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6387b-120">-DefaultProfile</span></span>
<span data-ttu-id="6387b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6387b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6387b-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6387b-122">-EmailAddress</span></span>
<span data-ttu-id="6387b-123">전자 메일 받는 사람에 대 한 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-124">-EmailReceiver</span></span>
<span data-ttu-id="6387b-125">전자 메일 받는 사람 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="6387b-126">-Name</span></span>
<span data-ttu-id="6387b-127">수신자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-127">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6387b-128">-PhoneNumber</span></span>
<span data-ttu-id="6387b-129">SMS 받는 사람에 대 한 전화 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6387b-130">-ServiceUri</span></span>
<span data-ttu-id="6387b-131">Webhook 수신기에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-132">-SmsReceiver</span></span>
<span data-ttu-id="6387b-133">SMS 받는 사람 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6387b-134">-WebhookReceiver</span></span>
<span data-ttu-id="6387b-135">Webhook 수신기를 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6387b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6387b-136">CommonParameters</span></span>
<span data-ttu-id="6387b-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6387b-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6387b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6387b-139">입력</span><span class="sxs-lookup"><span data-stu-id="6387b-139">INPUTS</span></span>

### <span data-ttu-id="6387b-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6387b-140">System.String</span></span>

### <span data-ttu-id="6387b-141">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6387b-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6387b-142">출력</span><span class="sxs-lookup"><span data-stu-id="6387b-142">OUTPUTS</span></span>

### <span data-ttu-id="6387b-143">PSActionGroupReceiverBase를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6387b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="6387b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6387b-144">NOTES</span></span>

## <span data-ttu-id="6387b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6387b-145">RELATED LINKS</span></span>

<span data-ttu-id="6387b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [제거-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="6387b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
