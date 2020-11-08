---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045805"
---
# <span data-ttu-id="4833a-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4833a-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="4833a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4833a-102">SYNOPSIS</span></span>

## <span data-ttu-id="4833a-103">구문과</span><span class="sxs-lookup"><span data-stu-id="4833a-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4833a-104">설명은</span><span class="sxs-lookup"><span data-stu-id="4833a-104">DESCRIPTION</span></span>

## <span data-ttu-id="4833a-105">예제의</span><span class="sxs-lookup"><span data-stu-id="4833a-105">EXAMPLES</span></span>

### <span data-ttu-id="4833a-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="4833a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4833a-107">변수</span><span class="sxs-lookup"><span data-stu-id="4833a-107">PARAMETERS</span></span>

### <span data-ttu-id="4833a-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4833a-108">-InformationAction</span></span>
<span data-ttu-id="4833a-109">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4833a-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4833a-110">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4833a-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4833a-111">하기로</span><span class="sxs-lookup"><span data-stu-id="4833a-111">Continue</span></span>
- <span data-ttu-id="4833a-112">숨기기</span><span class="sxs-lookup"><span data-stu-id="4833a-112">Ignore</span></span>
- <span data-ttu-id="4833a-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="4833a-113">Inquire</span></span>
- <span data-ttu-id="4833a-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4833a-114">SilentlyContinue</span></span>
- <span data-ttu-id="4833a-115">중지가</span><span class="sxs-lookup"><span data-stu-id="4833a-115">Stop</span></span>
- <span data-ttu-id="4833a-116">대기</span><span class="sxs-lookup"><span data-stu-id="4833a-116">Suspend</span></span>

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

### <span data-ttu-id="4833a-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4833a-117">-InformationVariable</span></span>
<span data-ttu-id="4833a-118">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4833a-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4833a-119">-IPForwarding 전환</span><span class="sxs-lookup"><span data-stu-id="4833a-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4833a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4833a-120">-Name</span></span>
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

### <span data-ttu-id="4833a-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4833a-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4833a-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="4833a-122">-Profile</span></span>
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

### <span data-ttu-id="4833a-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="4833a-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4833a-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4833a-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4833a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="4833a-125">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4833a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4833a-126">CommonParameters</span></span>
<span data-ttu-id="4833a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4833a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4833a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4833a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4833a-129">입력</span><span class="sxs-lookup"><span data-stu-id="4833a-129">INPUTS</span></span>

## <span data-ttu-id="4833a-130">출력</span><span class="sxs-lookup"><span data-stu-id="4833a-130">OUTPUTS</span></span>

## <span data-ttu-id="4833a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4833a-131">NOTES</span></span>

## <span data-ttu-id="4833a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4833a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4833a-133">추가-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4833a-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="4833a-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4833a-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="4833a-135">제거-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="4833a-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


