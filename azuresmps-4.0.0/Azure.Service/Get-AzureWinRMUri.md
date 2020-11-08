---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046505"
---
# <span data-ttu-id="8eafd-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="8eafd-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="8eafd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eafd-102">SYNOPSIS</span></span>
<span data-ttu-id="8eafd-103">가상 컴퓨터 또는 호스팅된 서비스의 가상 컴퓨터 목록에 대 한 WinRM https 수신기의 URI를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="8eafd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eafd-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8eafd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8eafd-105">DESCRIPTION</span></span>
<span data-ttu-id="8eafd-106">**Get-AzureWinRMUri** cmdlet은 가상 컴퓨터 또는 호스팅된 서비스의 가상 컴퓨터 목록에 대 한 WinRM (Windows Remote Management) https 수신기의 URI를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="8eafd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8eafd-107">EXAMPLES</span></span>

### <span data-ttu-id="8eafd-108">예제 1: 가상 컴퓨터에 대 한 WinRM https 수신기의 URI 가져오기</span><span class="sxs-lookup"><span data-stu-id="8eafd-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="8eafd-109">이 명령은 가상 컴퓨터에 대 한 WinRM https 수신기의 UIR을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="8eafd-110">예제 2: WinRM https 수신기의 URI를 특정 서비스의 가상 컴퓨터로 가져오기</span><span class="sxs-lookup"><span data-stu-id="8eafd-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="8eafd-111">이 명령은 가상 컴퓨터에 대 한 WinRM https 수신기의 UIR을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="8eafd-112">변수</span><span class="sxs-lookup"><span data-stu-id="8eafd-112">PARAMETERS</span></span>

### <span data-ttu-id="8eafd-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8eafd-113">-InformationAction</span></span>
<span data-ttu-id="8eafd-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8eafd-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8eafd-116">하기로</span><span class="sxs-lookup"><span data-stu-id="8eafd-116">Continue</span></span>
- <span data-ttu-id="8eafd-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="8eafd-117">Ignore</span></span>
- <span data-ttu-id="8eafd-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="8eafd-118">Inquire</span></span>
- <span data-ttu-id="8eafd-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8eafd-119">SilentlyContinue</span></span>
- <span data-ttu-id="8eafd-120">중지가</span><span class="sxs-lookup"><span data-stu-id="8eafd-120">Stop</span></span>
- <span data-ttu-id="8eafd-121">대기</span><span class="sxs-lookup"><span data-stu-id="8eafd-121">Suspend</span></span>

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

### <span data-ttu-id="8eafd-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8eafd-122">-InformationVariable</span></span>
<span data-ttu-id="8eafd-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8eafd-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8eafd-124">-Name</span></span>
<span data-ttu-id="8eafd-125">WinRM URI가 생성 되는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eafd-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="8eafd-126">-Profile</span></span>
<span data-ttu-id="8eafd-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8eafd-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8eafd-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8eafd-129">-ServiceName</span></span>
<span data-ttu-id="8eafd-130">가상 컴퓨터를 호스트 하는 Microsoft Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eafd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eafd-131">CommonParameters</span></span>
<span data-ttu-id="8eafd-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eafd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eafd-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eafd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eafd-134">입력</span><span class="sxs-lookup"><span data-stu-id="8eafd-134">INPUTS</span></span>

## <span data-ttu-id="8eafd-135">출력</span><span class="sxs-lookup"><span data-stu-id="8eafd-135">OUTPUTS</span></span>

## <span data-ttu-id="8eafd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8eafd-136">NOTES</span></span>

## <span data-ttu-id="8eafd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eafd-137">RELATED LINKS</span></span>

[<span data-ttu-id="8eafd-138">뉴욕</span><span class="sxs-lookup"><span data-stu-id="8eafd-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="8eafd-139">새로운 AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="8eafd-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


