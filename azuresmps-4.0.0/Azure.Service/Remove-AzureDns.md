---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046479"
---
# <span data-ttu-id="45c51-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="45c51-101">Remove-AzureDns</span></span>

## <span data-ttu-id="45c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c51-102">SYNOPSIS</span></span>
<span data-ttu-id="45c51-103">Azure 서비스에서 DNS 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="45c51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45c51-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="45c51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45c51-105">DESCRIPTION</span></span>
<span data-ttu-id="45c51-106">**제거-AzureDns** Cmdlet은 Azure 서비스에서 DNS 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="45c51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45c51-107">EXAMPLES</span></span>

### <span data-ttu-id="45c51-108">예제 1: 서비스에서 DNS 서버 제거</span><span class="sxs-lookup"><span data-stu-id="45c51-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="45c51-109">이 명령은 Dns07 이라는 DNS 서버를 ContosoService에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="45c51-110">변수</span><span class="sxs-lookup"><span data-stu-id="45c51-110">PARAMETERS</span></span>

### <span data-ttu-id="45c51-111">-Force</span><span class="sxs-lookup"><span data-stu-id="45c51-111">-Force</span></span>
<span data-ttu-id="45c51-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c51-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="45c51-113">-InformationAction</span></span>
<span data-ttu-id="45c51-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="45c51-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45c51-116">하기로</span><span class="sxs-lookup"><span data-stu-id="45c51-116">Continue</span></span>
- <span data-ttu-id="45c51-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="45c51-117">Ignore</span></span>
- <span data-ttu-id="45c51-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="45c51-118">Inquire</span></span>
- <span data-ttu-id="45c51-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="45c51-119">SilentlyContinue</span></span>
- <span data-ttu-id="45c51-120">중지가</span><span class="sxs-lookup"><span data-stu-id="45c51-120">Stop</span></span>
- <span data-ttu-id="45c51-121">대기</span><span class="sxs-lookup"><span data-stu-id="45c51-121">Suspend</span></span>

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

### <span data-ttu-id="45c51-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="45c51-122">-InformationVariable</span></span>
<span data-ttu-id="45c51-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="45c51-124">-이름</span><span class="sxs-lookup"><span data-stu-id="45c51-124">-Name</span></span>
<span data-ttu-id="45c51-125">이 cmdlet이 제거할 DNS 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45c51-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="45c51-126">-Profile</span></span>
<span data-ttu-id="45c51-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45c51-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45c51-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="45c51-129">-ServiceName</span></span>
<span data-ttu-id="45c51-130">이 cmdlet에서 DNS 서버를 제거 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="45c51-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c51-131">CommonParameters</span></span>
<span data-ttu-id="45c51-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c51-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c51-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c51-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c51-134">입력</span><span class="sxs-lookup"><span data-stu-id="45c51-134">INPUTS</span></span>

## <span data-ttu-id="45c51-135">출력</span><span class="sxs-lookup"><span data-stu-id="45c51-135">OUTPUTS</span></span>

### <span data-ttu-id="45c51-136">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="45c51-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="45c51-137">상속자</span><span class="sxs-lookup"><span data-stu-id="45c51-137">NOTES</span></span>

## <span data-ttu-id="45c51-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45c51-138">RELATED LINKS</span></span>

[<span data-ttu-id="45c51-139">추가-AzureDns</span><span class="sxs-lookup"><span data-stu-id="45c51-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="45c51-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="45c51-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="45c51-141">새 AzureDns</span><span class="sxs-lookup"><span data-stu-id="45c51-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="45c51-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="45c51-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


