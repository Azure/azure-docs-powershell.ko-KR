---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045756"
---
# <span data-ttu-id="ce599-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ce599-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="ce599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce599-102">SYNOPSIS</span></span>

## <span data-ttu-id="ce599-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ce599-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce599-104">설명은</span><span class="sxs-lookup"><span data-stu-id="ce599-104">DESCRIPTION</span></span>

## <span data-ttu-id="ce599-105">예제의</span><span class="sxs-lookup"><span data-stu-id="ce599-105">EXAMPLES</span></span>

### <span data-ttu-id="ce599-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="ce599-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ce599-107">변수</span><span class="sxs-lookup"><span data-stu-id="ce599-107">PARAMETERS</span></span>

### <span data-ttu-id="ce599-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ce599-108">-InformationAction</span></span>
<span data-ttu-id="ce599-109">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce599-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ce599-110">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ce599-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce599-111">하기로</span><span class="sxs-lookup"><span data-stu-id="ce599-111">Continue</span></span>
- <span data-ttu-id="ce599-112">숨기기</span><span class="sxs-lookup"><span data-stu-id="ce599-112">Ignore</span></span>
- <span data-ttu-id="ce599-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="ce599-113">Inquire</span></span>
- <span data-ttu-id="ce599-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ce599-114">SilentlyContinue</span></span>
- <span data-ttu-id="ce599-115">중지가</span><span class="sxs-lookup"><span data-stu-id="ce599-115">Stop</span></span>
- <span data-ttu-id="ce599-116">대기</span><span class="sxs-lookup"><span data-stu-id="ce599-116">Suspend</span></span>

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

### <span data-ttu-id="ce599-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ce599-117">-InformationVariable</span></span>
<span data-ttu-id="ce599-118">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce599-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ce599-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="ce599-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="ce599-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="ce599-120">-Profile</span></span>
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

### <span data-ttu-id="ce599-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ce599-121">-VM</span></span>
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

### <span data-ttu-id="ce599-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce599-122">CommonParameters</span></span>
<span data-ttu-id="ce599-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce599-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce599-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce599-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce599-125">입력</span><span class="sxs-lookup"><span data-stu-id="ce599-125">INPUTS</span></span>

## <span data-ttu-id="ce599-126">출력</span><span class="sxs-lookup"><span data-stu-id="ce599-126">OUTPUTS</span></span>

## <span data-ttu-id="ce599-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ce599-127">NOTES</span></span>

## <span data-ttu-id="ce599-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce599-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce599-129">제거-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ce599-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


