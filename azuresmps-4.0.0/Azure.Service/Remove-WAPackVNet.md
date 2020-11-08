---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047406"
---
# <span data-ttu-id="6e619-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6e619-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="6e619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e619-102">SYNOPSIS</span></span>
<span data-ttu-id="6e619-103">가상 네트워크 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="6e619-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e619-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e619-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e619-105">DESCRIPTION</span></span>
<span data-ttu-id="6e619-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="6e619-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e619-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e619-109">**Remove-WAPackVNet** cmdlet은 가상 네트워크 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="6e619-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6e619-110">EXAMPLES</span></span>

### <span data-ttu-id="6e619-111">예제 1: 가상화 된 네트워크 제거</span><span class="sxs-lookup"><span data-stu-id="6e619-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="6e619-112">첫 번째 명령은 **Get-help Apackvnet** cmdlet을 사용 하 여 ContosoVNet01 이라는 가상화 된 네트워크를 가져온 다음 해당 개체를 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="6e619-113">두 번째 명령은 $VNet에 저장 되어 있는 가상화 된 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="6e619-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6e619-115">예제 2: 확인 하지 않고 가상화 된 네트워크 제거</span><span class="sxs-lookup"><span data-stu-id="6e619-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="6e619-116">첫 번째 명령은 ContosoVNet02 ( **Get-WAPackVNet** cmdlet을 사용 하 여 명명 된 클라우드 서비스를 가져온 다음 해당 개체를 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="6e619-117">두 번째 명령은 $VNet에 저장 되어 있는 가상화 된 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="6e619-118">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="6e619-119">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e619-120">변수</span><span class="sxs-lookup"><span data-stu-id="6e619-120">PARAMETERS</span></span>

### <span data-ttu-id="6e619-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6e619-121">-Force</span></span>
<span data-ttu-id="6e619-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e619-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e619-123">-PassThru</span></span>
<span data-ttu-id="6e619-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e619-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e619-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="6e619-126">-Profile</span></span>
<span data-ttu-id="6e619-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e619-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e619-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="6e619-129">-VNet</span></span>
<span data-ttu-id="6e619-130">가상화 된 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="6e619-131">가상 네트워크를 얻으려면 **Get WAPackVNet** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e619-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e619-132">CommonParameters</span></span>
<span data-ttu-id="6e619-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e619-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e619-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e619-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e619-135">입력</span><span class="sxs-lookup"><span data-stu-id="6e619-135">INPUTS</span></span>

## <span data-ttu-id="6e619-136">출력</span><span class="sxs-lookup"><span data-stu-id="6e619-136">OUTPUTS</span></span>

## <span data-ttu-id="6e619-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6e619-137">NOTES</span></span>

## <span data-ttu-id="6e619-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e619-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e619-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6e619-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="6e619-140">새-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6e619-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


