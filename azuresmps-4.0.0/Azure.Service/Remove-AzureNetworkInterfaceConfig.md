---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046466"
---
# <span data-ttu-id="13f40-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="13f40-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="13f40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f40-102">SYNOPSIS</span></span>

## <span data-ttu-id="13f40-103">구문과</span><span class="sxs-lookup"><span data-stu-id="13f40-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13f40-104">설명은</span><span class="sxs-lookup"><span data-stu-id="13f40-104">DESCRIPTION</span></span>

## <span data-ttu-id="13f40-105">예제의</span><span class="sxs-lookup"><span data-stu-id="13f40-105">EXAMPLES</span></span>

### <span data-ttu-id="13f40-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="13f40-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="13f40-107">변수</span><span class="sxs-lookup"><span data-stu-id="13f40-107">PARAMETERS</span></span>

### <span data-ttu-id="13f40-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13f40-108">-InformationAction</span></span>
<span data-ttu-id="13f40-109">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f40-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13f40-110">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="13f40-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13f40-111">하기로</span><span class="sxs-lookup"><span data-stu-id="13f40-111">Continue</span></span>
- <span data-ttu-id="13f40-112">숨기기</span><span class="sxs-lookup"><span data-stu-id="13f40-112">Ignore</span></span>
- <span data-ttu-id="13f40-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="13f40-113">Inquire</span></span>
- <span data-ttu-id="13f40-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13f40-114">SilentlyContinue</span></span>
- <span data-ttu-id="13f40-115">중지가</span><span class="sxs-lookup"><span data-stu-id="13f40-115">Stop</span></span>
- <span data-ttu-id="13f40-116">대기</span><span class="sxs-lookup"><span data-stu-id="13f40-116">Suspend</span></span>

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

### <span data-ttu-id="13f40-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13f40-117">-InformationVariable</span></span>
<span data-ttu-id="13f40-118">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f40-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13f40-119">-이름</span><span class="sxs-lookup"><span data-stu-id="13f40-119">-Name</span></span>
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

### <span data-ttu-id="13f40-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="13f40-120">-Profile</span></span>
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

### <span data-ttu-id="13f40-121">-VM</span><span class="sxs-lookup"><span data-stu-id="13f40-121">-VM</span></span>
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

### <span data-ttu-id="13f40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f40-122">CommonParameters</span></span>
<span data-ttu-id="13f40-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f40-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f40-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f40-125">입력</span><span class="sxs-lookup"><span data-stu-id="13f40-125">INPUTS</span></span>

## <span data-ttu-id="13f40-126">출력</span><span class="sxs-lookup"><span data-stu-id="13f40-126">OUTPUTS</span></span>

## <span data-ttu-id="13f40-127">상속자</span><span class="sxs-lookup"><span data-stu-id="13f40-127">NOTES</span></span>

## <span data-ttu-id="13f40-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13f40-128">RELATED LINKS</span></span>

[<span data-ttu-id="13f40-129">추가-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="13f40-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="13f40-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="13f40-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="13f40-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="13f40-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


