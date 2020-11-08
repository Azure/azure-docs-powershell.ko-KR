---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045791"
---
# <span data-ttu-id="60b4b-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="60b4b-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="60b4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="60b4b-103">Azure 가상 컴퓨터의 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="60b4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60b4b-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="60b4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="60b4b-106">**AzureVMSize** cmdlet은 가상 컴퓨터의 크기를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="60b4b-107">이 파일에는 가상 컴퓨터의 새 크기인 *InstanceSize* 와 **get-help** cmdlet을 사용 하 여 검색 되는 가상 머신 개체인 *VM* 이라는 두 개의 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="60b4b-108">**Set-AzureVMSize** 결과를 **업데이트-add-azurevm** cmdlet으로 파이프 하거나 나중에 사용 하기 위해 변수에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="60b4b-109">**업데이트-add-azurevm** 를 실행할 때 까지는 실제 변경 내용이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="60b4b-110">참고:이 cmdlet은 가상 컴퓨터를 다시 프로 비전 해야 하며 새 IP 주소를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="60b4b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="60b4b-111">EXAMPLES</span></span>

### <span data-ttu-id="60b4b-112">예제 1: 가상 컴퓨터의 크기 설정</span><span class="sxs-lookup"><span data-stu-id="60b4b-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="60b4b-113">이 명령은 가상 컴퓨터를 "Small" 크기로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="60b4b-114">변수</span><span class="sxs-lookup"><span data-stu-id="60b4b-114">PARAMETERS</span></span>

### <span data-ttu-id="60b4b-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="60b4b-115">-InformationAction</span></span>
<span data-ttu-id="60b4b-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="60b4b-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60b4b-118">하기로</span><span class="sxs-lookup"><span data-stu-id="60b4b-118">Continue</span></span>
- <span data-ttu-id="60b4b-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="60b4b-119">Ignore</span></span>
- <span data-ttu-id="60b4b-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="60b4b-120">Inquire</span></span>
- <span data-ttu-id="60b4b-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="60b4b-121">SilentlyContinue</span></span>
- <span data-ttu-id="60b4b-122">중지가</span><span class="sxs-lookup"><span data-stu-id="60b4b-122">Stop</span></span>
- <span data-ttu-id="60b4b-123">대기</span><span class="sxs-lookup"><span data-stu-id="60b4b-123">Suspend</span></span>

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

### <span data-ttu-id="60b4b-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="60b4b-124">-InformationVariable</span></span>
<span data-ttu-id="60b4b-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="60b4b-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="60b4b-126">-InstanceSize</span></span>
<span data-ttu-id="60b4b-127">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="60b4b-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="60b4b-129">--ExtraSmall--작음--보통--큼--높음--ExtraLarge--A5--A6--A7</span><span class="sxs-lookup"><span data-stu-id="60b4b-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b4b-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="60b4b-130">-Profile</span></span>
<span data-ttu-id="60b4b-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60b4b-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60b4b-133">-VM</span><span class="sxs-lookup"><span data-stu-id="60b4b-133">-VM</span></span>
<span data-ttu-id="60b4b-134">이 cmdlet이 크기를 설정 하는 영구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="60b4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b4b-135">CommonParameters</span></span>
<span data-ttu-id="60b4b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b4b-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b4b-138">입력</span><span class="sxs-lookup"><span data-stu-id="60b4b-138">INPUTS</span></span>

## <span data-ttu-id="60b4b-139">출력</span><span class="sxs-lookup"><span data-stu-id="60b4b-139">OUTPUTS</span></span>

## <span data-ttu-id="60b4b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="60b4b-140">NOTES</span></span>

## <span data-ttu-id="60b4b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60b4b-141">RELATED LINKS</span></span>

[<span data-ttu-id="60b4b-142">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="60b4b-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="60b4b-143">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="60b4b-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


