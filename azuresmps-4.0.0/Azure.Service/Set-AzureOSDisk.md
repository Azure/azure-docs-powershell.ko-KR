---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045828"
---
# <span data-ttu-id="64320-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="64320-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="64320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64320-102">SYNOPSIS</span></span>
<span data-ttu-id="64320-103">Azure 가상 컴퓨터의 호스트 캐시 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="64320-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64320-104">SYNTAX</span></span>

### <span data-ttu-id="64320-105">로이 Esize</span><span class="sxs-lookup"><span data-stu-id="64320-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="64320-106">길이</span><span class="sxs-lookup"><span data-stu-id="64320-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="64320-107">설명은</span><span class="sxs-lookup"><span data-stu-id="64320-107">DESCRIPTION</span></span>
<span data-ttu-id="64320-108">**AzureOSDisk** Cmdlet은 Azure 가상 컴퓨터의 운영 체제 디스크에 대 한 호스트 캐시 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="64320-109">지원 되는 호스트 캐시 모드는 ReadOnly 및 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="64320-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="64320-110">실행 중인 가상 컴퓨터에서이 cmdlet을 실행 하면 해당 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64320-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="64320-111">예제의</span><span class="sxs-lookup"><span data-stu-id="64320-111">EXAMPLES</span></span>

### <span data-ttu-id="64320-112">예제 1: 파이프라인을 사용 하 여 호스트 캐시 모드를 ReadOnly로 설정</span><span class="sxs-lookup"><span data-stu-id="64320-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="64320-113">이 명령은 VirtualMachine02 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="64320-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="64320-114">이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64320-115">현재 cmdlet은 해당 가상 컴퓨터의 운영 체제 디스크에 대 한 호스트 캐시 모드를 읽기 전용으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="64320-116">예제 2: 호스트 캐시 모드를 ReadWrite로 설정</span><span class="sxs-lookup"><span data-stu-id="64320-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="64320-117">첫 번째 명령은 ContosoService 이라는 서비스에서 VirtualMachine02 이라는 가상 컴퓨터를 가져온 다음 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="64320-118">두 번째 명령은 해당 가상 컴퓨터의 운영 체제 디스크 호스트 캐시 모드를 ReadWrite로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="64320-119">변수</span><span class="sxs-lookup"><span data-stu-id="64320-119">PARAMETERS</span></span>

### <span data-ttu-id="64320-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="64320-120">-HostCaching</span></span>
<span data-ttu-id="64320-121">운영 체제 디스크에 대 한 호스트 캐시 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="64320-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64320-122">Valid values are:</span></span> 

- <span data-ttu-id="64320-123">읽기</span><span class="sxs-lookup"><span data-stu-id="64320-123">ReadOnly</span></span> 
- <span data-ttu-id="64320-124">쓰기</span><span class="sxs-lookup"><span data-stu-id="64320-124">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64320-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="64320-125">-InformationAction</span></span>
<span data-ttu-id="64320-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="64320-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64320-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64320-128">하기로</span><span class="sxs-lookup"><span data-stu-id="64320-128">Continue</span></span>
- <span data-ttu-id="64320-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="64320-129">Ignore</span></span>
- <span data-ttu-id="64320-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="64320-130">Inquire</span></span>
- <span data-ttu-id="64320-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="64320-131">SilentlyContinue</span></span>
- <span data-ttu-id="64320-132">중지가</span><span class="sxs-lookup"><span data-stu-id="64320-132">Stop</span></span>
- <span data-ttu-id="64320-133">대기</span><span class="sxs-lookup"><span data-stu-id="64320-133">Suspend</span></span>

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

### <span data-ttu-id="64320-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="64320-134">-InformationVariable</span></span>
<span data-ttu-id="64320-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="64320-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="64320-136">-Profile</span></span>
<span data-ttu-id="64320-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64320-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="64320-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64320-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="64320-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="64320-140">운영 체제 디스크의 새 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="64320-141">크기는 현재 크기 보다 커야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64320-142">-VM</span><span class="sxs-lookup"><span data-stu-id="64320-142">-VM</span></span>
<span data-ttu-id="64320-143">이 cmdlet이 운영 체제 디스크를 수정 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="64320-144">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="64320-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64320-145">CommonParameters</span></span>
<span data-ttu-id="64320-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64320-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64320-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64320-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64320-148">입력</span><span class="sxs-lookup"><span data-stu-id="64320-148">INPUTS</span></span>

## <span data-ttu-id="64320-149">출력</span><span class="sxs-lookup"><span data-stu-id="64320-149">OUTPUTS</span></span>

## <span data-ttu-id="64320-150">상속자</span><span class="sxs-lookup"><span data-stu-id="64320-150">NOTES</span></span>

## <span data-ttu-id="64320-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64320-151">RELATED LINKS</span></span>

[<span data-ttu-id="64320-152">추가-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="64320-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="64320-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="64320-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="64320-154">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="64320-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="64320-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="64320-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="64320-156">Set AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="64320-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="64320-157">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="64320-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


