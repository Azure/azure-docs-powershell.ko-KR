---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045924"
---
# <span data-ttu-id="ede83-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="ede83-101">New-AzureDns</span></span>

## <span data-ttu-id="ede83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede83-102">SYNOPSIS</span></span>
<span data-ttu-id="ede83-103">Azure DNS settings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="ede83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ede83-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ede83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ede83-105">DESCRIPTION</span></span>
<span data-ttu-id="ede83-106">**새로운 azuredns** Cmdlet은 Azure dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="ede83-107">**새 add-azurevm** cmdlet을 사용 하 여 가상 컴퓨터를 만들 때 DNS 설정 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="ede83-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ede83-108">EXAMPLES</span></span>

### <span data-ttu-id="ede83-109">예제 1: DNS 설정 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ede83-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="ede83-110">이 명령은 Azure DNS 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="ede83-111">DNS 서버에는 지정 된 주소와 친근 한 이름 Dns01 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="ede83-112">이 명령은 **새 add-azurevm** cmdlet에서 사용할 개체를 $Dns 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="ede83-113">변수</span><span class="sxs-lookup"><span data-stu-id="ede83-113">PARAMETERS</span></span>

### <span data-ttu-id="ede83-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ede83-114">-InformationAction</span></span>
<span data-ttu-id="ede83-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ede83-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ede83-117">하기로</span><span class="sxs-lookup"><span data-stu-id="ede83-117">Continue</span></span>
- <span data-ttu-id="ede83-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="ede83-118">Ignore</span></span>
- <span data-ttu-id="ede83-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="ede83-119">Inquire</span></span>
- <span data-ttu-id="ede83-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ede83-120">SilentlyContinue</span></span>
- <span data-ttu-id="ede83-121">중지가</span><span class="sxs-lookup"><span data-stu-id="ede83-121">Stop</span></span>
- <span data-ttu-id="ede83-122">대기</span><span class="sxs-lookup"><span data-stu-id="ede83-122">Suspend</span></span>

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

### <span data-ttu-id="ede83-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ede83-123">-InformationVariable</span></span>
<span data-ttu-id="ede83-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ede83-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ede83-125">-IPAddress</span></span>
<span data-ttu-id="ede83-126">DNS 서버의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-126">Specifies the IP address of the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede83-127">-이름</span><span class="sxs-lookup"><span data-stu-id="ede83-127">-Name</span></span>
<span data-ttu-id="ede83-128">DNS 서버에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="ede83-129">이 이름은 완전히 정규화 된 도메인 이름이 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-129">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede83-130">CommonParameters</span></span>
<span data-ttu-id="ede83-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede83-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede83-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede83-133">입력</span><span class="sxs-lookup"><span data-stu-id="ede83-133">INPUTS</span></span>

## <span data-ttu-id="ede83-134">출력</span><span class="sxs-lookup"><span data-stu-id="ede83-134">OUTPUTS</span></span>

## <span data-ttu-id="ede83-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ede83-135">NOTES</span></span>

## <span data-ttu-id="ede83-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ede83-136">RELATED LINKS</span></span>

[<span data-ttu-id="ede83-137">추가-AzureDns</span><span class="sxs-lookup"><span data-stu-id="ede83-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="ede83-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="ede83-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="ede83-139">뉴욕</span><span class="sxs-lookup"><span data-stu-id="ede83-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ede83-140">-AzureDns 제거</span><span class="sxs-lookup"><span data-stu-id="ede83-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="ede83-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="ede83-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


