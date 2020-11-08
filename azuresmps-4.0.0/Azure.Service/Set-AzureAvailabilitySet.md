---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046067"
---
# <span data-ttu-id="f2225-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2225-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="f2225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2225-102">SYNOPSIS</span></span>
<span data-ttu-id="f2225-103">Azure 가상 머신에서 가용성 집합의 이름을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="f2225-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2225-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2225-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2225-105">DESCRIPTION</span></span>
<span data-ttu-id="f2225-106">**AzureAvailabilitySet** cmdlet은 배포 후 Azure 가상 컴퓨터에서 가용성 집합의 이름을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="f2225-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2225-107">EXAMPLES</span></span>

### <span data-ttu-id="f2225-108">예제 1: 가용성 집합 이름 수정</span><span class="sxs-lookup"><span data-stu-id="f2225-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="f2225-109">첫 번째 명령은 **VirtualMachine07 cmdlet을 사용 하 여 ContosoService** 이라는 이름의 서비스에서 가상 컴퓨터 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f2225-110">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2225-111">해당 cmdlet은 해당 가상 컴퓨터에 대 한 가용성 집합의 이름을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="f2225-112">명령이 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="f2225-113">변수</span><span class="sxs-lookup"><span data-stu-id="f2225-113">PARAMETERS</span></span>

### <span data-ttu-id="f2225-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="f2225-114">-AvailabilitySetName</span></span>
<span data-ttu-id="f2225-115">가상 머신이 속한 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2225-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2225-116">-InformationAction</span></span>
<span data-ttu-id="f2225-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2225-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2225-119">하기로</span><span class="sxs-lookup"><span data-stu-id="f2225-119">Continue</span></span>
- <span data-ttu-id="f2225-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="f2225-120">Ignore</span></span>
- <span data-ttu-id="f2225-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="f2225-121">Inquire</span></span>
- <span data-ttu-id="f2225-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2225-122">SilentlyContinue</span></span>
- <span data-ttu-id="f2225-123">중지가</span><span class="sxs-lookup"><span data-stu-id="f2225-123">Stop</span></span>
- <span data-ttu-id="f2225-124">대기</span><span class="sxs-lookup"><span data-stu-id="f2225-124">Suspend</span></span>

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

### <span data-ttu-id="f2225-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2225-125">-InformationVariable</span></span>
<span data-ttu-id="f2225-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2225-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="f2225-127">-Profile</span></span>
<span data-ttu-id="f2225-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2225-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2225-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f2225-130">-VM</span></span>
<span data-ttu-id="f2225-131">이 cmdlet이 수정 하는 가상 컴퓨터 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f2225-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2225-132">CommonParameters</span></span>
<span data-ttu-id="f2225-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2225-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2225-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2225-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2225-135">입력</span><span class="sxs-lookup"><span data-stu-id="f2225-135">INPUTS</span></span>

## <span data-ttu-id="f2225-136">출력</span><span class="sxs-lookup"><span data-stu-id="f2225-136">OUTPUTS</span></span>

## <span data-ttu-id="f2225-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f2225-137">NOTES</span></span>

## <span data-ttu-id="f2225-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2225-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2225-139">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f2225-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f2225-140">제거-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2225-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


