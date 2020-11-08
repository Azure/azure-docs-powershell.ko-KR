---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046584"
---
# <span data-ttu-id="d83d0-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d83d0-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="d83d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83d0-102">SYNOPSIS</span></span>

## <span data-ttu-id="d83d0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="d83d0-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d83d0-104">설명은</span><span class="sxs-lookup"><span data-stu-id="d83d0-104">DESCRIPTION</span></span>

## <span data-ttu-id="d83d0-105">예제의</span><span class="sxs-lookup"><span data-stu-id="d83d0-105">EXAMPLES</span></span>

### <span data-ttu-id="d83d0-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="d83d0-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d83d0-107">변수</span><span class="sxs-lookup"><span data-stu-id="d83d0-107">PARAMETERS</span></span>

### <span data-ttu-id="d83d0-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d83d0-108">-InformationAction</span></span>
<span data-ttu-id="d83d0-109">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d83d0-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d83d0-110">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d83d0-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d83d0-111">하기로</span><span class="sxs-lookup"><span data-stu-id="d83d0-111">Continue</span></span>
- <span data-ttu-id="d83d0-112">숨기기</span><span class="sxs-lookup"><span data-stu-id="d83d0-112">Ignore</span></span>
- <span data-ttu-id="d83d0-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="d83d0-113">Inquire</span></span>
- <span data-ttu-id="d83d0-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d83d0-114">SilentlyContinue</span></span>
- <span data-ttu-id="d83d0-115">중지가</span><span class="sxs-lookup"><span data-stu-id="d83d0-115">Stop</span></span>
- <span data-ttu-id="d83d0-116">대기</span><span class="sxs-lookup"><span data-stu-id="d83d0-116">Suspend</span></span>

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

### <span data-ttu-id="d83d0-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d83d0-117">-InformationVariable</span></span>
<span data-ttu-id="d83d0-118">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d83d0-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d83d0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d83d0-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83d0-120">-VM</span><span class="sxs-lookup"><span data-stu-id="d83d0-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d83d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83d0-121">CommonParameters</span></span>
<span data-ttu-id="d83d0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d83d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83d0-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83d0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83d0-124">입력</span><span class="sxs-lookup"><span data-stu-id="d83d0-124">INPUTS</span></span>

## <span data-ttu-id="d83d0-125">출력</span><span class="sxs-lookup"><span data-stu-id="d83d0-125">OUTPUTS</span></span>

## <span data-ttu-id="d83d0-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d83d0-126">NOTES</span></span>

## <span data-ttu-id="d83d0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d83d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="d83d0-128">추가-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d83d0-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d83d0-129">제거-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d83d0-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d83d0-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d83d0-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


