---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045646"
---
# <span data-ttu-id="3d65f-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3d65f-101">Get-AzureDns</span></span>

## <span data-ttu-id="3d65f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d65f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d65f-103">Azure 배포에 대 한 DNS 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="3d65f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d65f-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d65f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d65f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d65f-106">**Get-azuredns** Cmdlet은 Azure 배포에 대 한 DNS 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="3d65f-107">Cmdlet은 dns 설정 개체에 DNS 서버의 이름 및 IP 주소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="3d65f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3d65f-108">EXAMPLES</span></span>

### <span data-ttu-id="3d65f-109">예제 1: DNS 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d65f-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="3d65f-110">이 명령은 **Get AzureDeployment** cmdlet을 사용 하 여 ContosoService 라는 서비스의 프로덕션 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="3d65f-111">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3d65f-112">현재 cmdlet은 DNS 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="3d65f-113">변수</span><span class="sxs-lookup"><span data-stu-id="3d65f-113">PARAMETERS</span></span>

### <span data-ttu-id="3d65f-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="3d65f-114">-DnsSettings</span></span>
<span data-ttu-id="3d65f-115">**DnsSettings** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d65f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d65f-116">-InformationAction</span></span>
<span data-ttu-id="3d65f-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d65f-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d65f-119">하기로</span><span class="sxs-lookup"><span data-stu-id="3d65f-119">Continue</span></span>
- <span data-ttu-id="3d65f-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="3d65f-120">Ignore</span></span>
- <span data-ttu-id="3d65f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="3d65f-121">Inquire</span></span>
- <span data-ttu-id="3d65f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d65f-122">SilentlyContinue</span></span>
- <span data-ttu-id="3d65f-123">중지가</span><span class="sxs-lookup"><span data-stu-id="3d65f-123">Stop</span></span>
- <span data-ttu-id="3d65f-124">대기</span><span class="sxs-lookup"><span data-stu-id="3d65f-124">Suspend</span></span>

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

### <span data-ttu-id="3d65f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d65f-125">-InformationVariable</span></span>
<span data-ttu-id="3d65f-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d65f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d65f-127">CommonParameters</span></span>
<span data-ttu-id="3d65f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d65f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d65f-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d65f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d65f-130">입력</span><span class="sxs-lookup"><span data-stu-id="3d65f-130">INPUTS</span></span>

## <span data-ttu-id="3d65f-131">출력</span><span class="sxs-lookup"><span data-stu-id="3d65f-131">OUTPUTS</span></span>

## <span data-ttu-id="3d65f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3d65f-132">NOTES</span></span>

## <span data-ttu-id="3d65f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d65f-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d65f-134">추가-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3d65f-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="3d65f-135">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3d65f-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="3d65f-136">새 AzureDns</span><span class="sxs-lookup"><span data-stu-id="3d65f-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="3d65f-137">-AzureDns 제거</span><span class="sxs-lookup"><span data-stu-id="3d65f-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="3d65f-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3d65f-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


