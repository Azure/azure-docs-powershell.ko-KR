---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046394"
---
# <span data-ttu-id="35032-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="35032-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="35032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35032-102">SYNOPSIS</span></span>

## <span data-ttu-id="35032-103">구문과</span><span class="sxs-lookup"><span data-stu-id="35032-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="35032-104">설명은</span><span class="sxs-lookup"><span data-stu-id="35032-104">DESCRIPTION</span></span>

## <span data-ttu-id="35032-105">예제의</span><span class="sxs-lookup"><span data-stu-id="35032-105">EXAMPLES</span></span>

### <span data-ttu-id="35032-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="35032-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="35032-107">변수</span><span class="sxs-lookup"><span data-stu-id="35032-107">PARAMETERS</span></span>

### <span data-ttu-id="35032-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="35032-108">-InformationAction</span></span>
<span data-ttu-id="35032-109">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35032-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="35032-110">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="35032-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35032-111">하기로</span><span class="sxs-lookup"><span data-stu-id="35032-111">Continue</span></span>
- <span data-ttu-id="35032-112">숨기기</span><span class="sxs-lookup"><span data-stu-id="35032-112">Ignore</span></span>
- <span data-ttu-id="35032-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="35032-113">Inquire</span></span>
- <span data-ttu-id="35032-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35032-114">SilentlyContinue</span></span>
- <span data-ttu-id="35032-115">중지가</span><span class="sxs-lookup"><span data-stu-id="35032-115">Stop</span></span>
- <span data-ttu-id="35032-116">대기</span><span class="sxs-lookup"><span data-stu-id="35032-116">Suspend</span></span>

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

### <span data-ttu-id="35032-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35032-117">-InformationVariable</span></span>
<span data-ttu-id="35032-118">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35032-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35032-119">-IPForwarding 전환</span><span class="sxs-lookup"><span data-stu-id="35032-119">-IPForwarding</span></span>
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

### <span data-ttu-id="35032-120">-이름</span><span class="sxs-lookup"><span data-stu-id="35032-120">-Name</span></span>
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

### <span data-ttu-id="35032-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35032-121">-NetworkSecurityGroup</span></span>
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

### <span data-ttu-id="35032-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="35032-122">-Profile</span></span>
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

### <span data-ttu-id="35032-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="35032-123">-StaticVNetIPAddress</span></span>
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

### <span data-ttu-id="35032-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="35032-124">-SubnetName</span></span>
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

### <span data-ttu-id="35032-125">-VM</span><span class="sxs-lookup"><span data-stu-id="35032-125">-VM</span></span>
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

### <span data-ttu-id="35032-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35032-126">CommonParameters</span></span>
<span data-ttu-id="35032-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35032-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35032-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35032-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35032-129">입력</span><span class="sxs-lookup"><span data-stu-id="35032-129">INPUTS</span></span>

## <span data-ttu-id="35032-130">출력</span><span class="sxs-lookup"><span data-stu-id="35032-130">OUTPUTS</span></span>

## <span data-ttu-id="35032-131">상속자</span><span class="sxs-lookup"><span data-stu-id="35032-131">NOTES</span></span>

## <span data-ttu-id="35032-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35032-132">RELATED LINKS</span></span>

[<span data-ttu-id="35032-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="35032-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="35032-134">제거-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="35032-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="35032-135">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="35032-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


