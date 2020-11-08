---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045494"
---
# <span data-ttu-id="e803a-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e803a-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="e803a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e803a-102">SYNOPSIS</span></span>
<span data-ttu-id="e803a-103">가상 컴퓨터 개체에서 Azure virtual machine SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="e803a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e803a-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e803a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e803a-105">DESCRIPTION</span></span>
<span data-ttu-id="e803a-106">**AzureVMSqlServerExtension** cmdlet은 가상 컴퓨터 개체에서 Azure VIRTUAL Machine SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="e803a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e803a-107">EXAMPLES</span></span>

### <span data-ttu-id="e803a-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="e803a-108">1:</span></span>
```

```

## <span data-ttu-id="e803a-109">변수</span><span class="sxs-lookup"><span data-stu-id="e803a-109">PARAMETERS</span></span>

### <span data-ttu-id="e803a-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e803a-110">-InformationAction</span></span>
<span data-ttu-id="e803a-111">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e803a-112">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e803a-113">하기로</span><span class="sxs-lookup"><span data-stu-id="e803a-113">Continue</span></span>
- <span data-ttu-id="e803a-114">숨기기</span><span class="sxs-lookup"><span data-stu-id="e803a-114">Ignore</span></span>
- <span data-ttu-id="e803a-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="e803a-115">Inquire</span></span>
- <span data-ttu-id="e803a-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e803a-116">SilentlyContinue</span></span>
- <span data-ttu-id="e803a-117">중지가</span><span class="sxs-lookup"><span data-stu-id="e803a-117">Stop</span></span>
- <span data-ttu-id="e803a-118">대기</span><span class="sxs-lookup"><span data-stu-id="e803a-118">Suspend</span></span>

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

### <span data-ttu-id="e803a-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e803a-119">-InformationVariable</span></span>
<span data-ttu-id="e803a-120">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e803a-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="e803a-121">-Profile</span></span>
<span data-ttu-id="e803a-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e803a-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e803a-124">-VM</span><span class="sxs-lookup"><span data-stu-id="e803a-124">-VM</span></span>
<span data-ttu-id="e803a-125">이 cmdlet에서 확장명을 제거 하는 영구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="e803a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e803a-126">CommonParameters</span></span>
<span data-ttu-id="e803a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e803a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e803a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e803a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e803a-129">입력</span><span class="sxs-lookup"><span data-stu-id="e803a-129">INPUTS</span></span>

## <span data-ttu-id="e803a-130">출력</span><span class="sxs-lookup"><span data-stu-id="e803a-130">OUTPUTS</span></span>

## <span data-ttu-id="e803a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e803a-131">NOTES</span></span>

## <span data-ttu-id="e803a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e803a-132">RELATED LINKS</span></span>

[<span data-ttu-id="e803a-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e803a-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e803a-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e803a-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


