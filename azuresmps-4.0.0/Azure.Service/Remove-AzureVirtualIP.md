---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045487"
---
# <span data-ttu-id="6eb81-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="6eb81-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="6eb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb81-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb81-103">클라우드 서비스에서 가상 IP 주소를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="6eb81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eb81-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6eb81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6eb81-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb81-106">**제거-AzureVirtualIP** Cmdlet은 Azure 서비스에서 VIP (가상 IP)를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="6eb81-107">가상 IP에 연결 된 끝점이 없는 경우에만 작업이 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="6eb81-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6eb81-108">EXAMPLES</span></span>

### <span data-ttu-id="6eb81-109">예제 1: 서비스에서 가상 IP 주소 제거</span><span class="sxs-lookup"><span data-stu-id="6eb81-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="6eb81-110">이 명령은 서비스에서 가상 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="6eb81-111">변수</span><span class="sxs-lookup"><span data-stu-id="6eb81-111">PARAMETERS</span></span>

### <span data-ttu-id="6eb81-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6eb81-112">-Force</span></span>
<span data-ttu-id="6eb81-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb81-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6eb81-114">-InformationAction</span></span>
<span data-ttu-id="6eb81-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6eb81-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6eb81-117">하기로</span><span class="sxs-lookup"><span data-stu-id="6eb81-117">Continue</span></span>
- <span data-ttu-id="6eb81-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="6eb81-118">Ignore</span></span>
- <span data-ttu-id="6eb81-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="6eb81-119">Inquire</span></span>
- <span data-ttu-id="6eb81-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6eb81-120">SilentlyContinue</span></span>
- <span data-ttu-id="6eb81-121">중지가</span><span class="sxs-lookup"><span data-stu-id="6eb81-121">Stop</span></span>
- <span data-ttu-id="6eb81-122">대기</span><span class="sxs-lookup"><span data-stu-id="6eb81-122">Suspend</span></span>

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

### <span data-ttu-id="6eb81-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6eb81-123">-InformationVariable</span></span>
<span data-ttu-id="6eb81-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6eb81-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="6eb81-125">-Profile</span></span>
<span data-ttu-id="6eb81-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6eb81-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6eb81-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6eb81-128">-ServiceName</span></span>
<span data-ttu-id="6eb81-129">가상 IP 주소를 제거할 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="6eb81-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="6eb81-130">-VirtualIPName</span></span>
<span data-ttu-id="6eb81-131">제거할 가상 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-131">Specifies the name of the virtual IP address to remove.</span></span>

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

### <span data-ttu-id="6eb81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb81-132">CommonParameters</span></span>
<span data-ttu-id="6eb81-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb81-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eb81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb81-135">입력</span><span class="sxs-lookup"><span data-stu-id="6eb81-135">INPUTS</span></span>

## <span data-ttu-id="6eb81-136">출력</span><span class="sxs-lookup"><span data-stu-id="6eb81-136">OUTPUTS</span></span>

### <span data-ttu-id="6eb81-137">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="6eb81-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="6eb81-138">상속자</span><span class="sxs-lookup"><span data-stu-id="6eb81-138">NOTES</span></span>

## <span data-ttu-id="6eb81-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eb81-139">RELATED LINKS</span></span>

[<span data-ttu-id="6eb81-140">추가-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="6eb81-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


