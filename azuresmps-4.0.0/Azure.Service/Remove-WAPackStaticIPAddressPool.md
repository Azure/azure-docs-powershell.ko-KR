---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047412"
---
# <span data-ttu-id="155dc-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="155dc-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="155dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="155dc-102">SYNOPSIS</span></span>
<span data-ttu-id="155dc-103">고정 IP 주소 풀 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="155dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="155dc-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="155dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="155dc-105">DESCRIPTION</span></span>
<span data-ttu-id="155dc-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="155dc-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="155dc-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="155dc-109">**WAPackStaticIPAddressPool** cmdlet은 정적 IP 주소 풀 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="155dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="155dc-110">EXAMPLES</span></span>

### <span data-ttu-id="155dc-111">예제 1: 고정 IP 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="155dc-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="155dc-112">첫 번째 명령은 **WAPackStaticIPAddressPool** cmdlet을 사용 하 여 ContosoStaticIPAddressPool01 이라는 고정 IP 주소 풀을 가져온 다음 해당 개체를 $StaticIPAddressPool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="155dc-113">두 번째 명령은 $StaticIPAddressPool에 저장 된 고정 IP 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="155dc-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="155dc-115">예제 2: 확인 없이 고정 IP 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="155dc-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="155dc-116">첫 번째 명령은 **WAPackStaticIPAddressPool** cmdlet을 사용 하 여 ContosoStaticIPAddressPool02 이라는 고정 IP 주소 풀을 가져온 다음 해당 개체를 $ StaticIPAddressPool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="155dc-117">두 번째 명령은 $StaticIPAddressPool에 저장 된 고정 IP 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="155dc-118">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="155dc-119">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="155dc-120">변수</span><span class="sxs-lookup"><span data-stu-id="155dc-120">PARAMETERS</span></span>

### <span data-ttu-id="155dc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="155dc-121">-Force</span></span>
<span data-ttu-id="155dc-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="155dc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="155dc-123">-PassThru</span></span>
<span data-ttu-id="155dc-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="155dc-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="155dc-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="155dc-126">-Profile</span></span>
<span data-ttu-id="155dc-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="155dc-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="155dc-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="155dc-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="155dc-130">StaticIPAddressPool를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="155dc-131">고정 IP 주소 풀을 얻으려면 **Get-WAPackStaticIPAddressPool** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="155dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155dc-132">CommonParameters</span></span>
<span data-ttu-id="155dc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="155dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155dc-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="155dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155dc-135">입력</span><span class="sxs-lookup"><span data-stu-id="155dc-135">INPUTS</span></span>

## <span data-ttu-id="155dc-136">출력</span><span class="sxs-lookup"><span data-stu-id="155dc-136">OUTPUTS</span></span>

## <span data-ttu-id="155dc-137">상속자</span><span class="sxs-lookup"><span data-stu-id="155dc-137">NOTES</span></span>

## <span data-ttu-id="155dc-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="155dc-138">RELATED LINKS</span></span>

[<span data-ttu-id="155dc-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="155dc-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="155dc-140">제거-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="155dc-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


