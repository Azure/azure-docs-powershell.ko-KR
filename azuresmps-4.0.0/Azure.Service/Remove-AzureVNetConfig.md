---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045492"
---
# <span data-ttu-id="3162f-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="3162f-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="3162f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3162f-102">SYNOPSIS</span></span>
<span data-ttu-id="3162f-103">현재 Azure 구독에서 네트워크 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="3162f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3162f-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3162f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3162f-105">DESCRIPTION</span></span>
<span data-ttu-id="3162f-106">**제거-AzureVNetConfig** cmdlet은 현재 Azure 구독에서 모든 가상 네트워크 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="3162f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3162f-107">EXAMPLES</span></span>

### <span data-ttu-id="3162f-108">예제 1: 현재 구독에서 가상 네트워크 구성 제거</span><span class="sxs-lookup"><span data-stu-id="3162f-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="3162f-109">이 명령은 현재 구독에서 가상 네트워크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="3162f-110">변수</span><span class="sxs-lookup"><span data-stu-id="3162f-110">PARAMETERS</span></span>

### <span data-ttu-id="3162f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3162f-111">-InformationAction</span></span>
<span data-ttu-id="3162f-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3162f-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3162f-114">하기로</span><span class="sxs-lookup"><span data-stu-id="3162f-114">Continue</span></span>
- <span data-ttu-id="3162f-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="3162f-115">Ignore</span></span>
- <span data-ttu-id="3162f-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="3162f-116">Inquire</span></span>
- <span data-ttu-id="3162f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3162f-117">SilentlyContinue</span></span>
- <span data-ttu-id="3162f-118">중지가</span><span class="sxs-lookup"><span data-stu-id="3162f-118">Stop</span></span>
- <span data-ttu-id="3162f-119">대기</span><span class="sxs-lookup"><span data-stu-id="3162f-119">Suspend</span></span>

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

### <span data-ttu-id="3162f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3162f-120">-InformationVariable</span></span>
<span data-ttu-id="3162f-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3162f-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="3162f-122">-Profile</span></span>
<span data-ttu-id="3162f-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3162f-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3162f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3162f-125">CommonParameters</span></span>
<span data-ttu-id="3162f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3162f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3162f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3162f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3162f-128">입력</span><span class="sxs-lookup"><span data-stu-id="3162f-128">INPUTS</span></span>

## <span data-ttu-id="3162f-129">출력</span><span class="sxs-lookup"><span data-stu-id="3162f-129">OUTPUTS</span></span>

## <span data-ttu-id="3162f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3162f-130">NOTES</span></span>

## <span data-ttu-id="3162f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3162f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3162f-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="3162f-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="3162f-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="3162f-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="3162f-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="3162f-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


