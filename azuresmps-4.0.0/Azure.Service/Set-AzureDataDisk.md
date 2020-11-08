---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046066"
---
# <span data-ttu-id="7fde7-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7fde7-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="7fde7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fde7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fde7-103">Azure 가상 머신에서 기존 데이터 디스크의 호스트 캐싱을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="7fde7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fde7-104">SYNTAX</span></span>

### <span data-ttu-id="7fde7-105">로이 Esize</span><span class="sxs-lookup"><span data-stu-id="7fde7-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fde7-106">길이</span><span class="sxs-lookup"><span data-stu-id="7fde7-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fde7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7fde7-107">DESCRIPTION</span></span>
<span data-ttu-id="7fde7-108">**Set AzureDataDisk** Cmdlet은 Azure 가상 머신에서 기존 데이터 디스크의 캐시 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="7fde7-109">LUN (논리 단위 번호)을 기준으로 업데이트할 데이터 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="7fde7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7fde7-110">EXAMPLES</span></span>

### <span data-ttu-id="7fde7-111">예제 1: 데이터 디스크에 대 한 호스트 캐싱 수정</span><span class="sxs-lookup"><span data-stu-id="7fde7-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="7fde7-112">이 명령은 **get-help** cmdlet을 사용 하 여 ContosoService 이라는 서비스에서 실행 되는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="7fde7-113">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7fde7-114">해당 cmdlet은 VirtualMachine07 이라는 가상 컴퓨터의 LUN 2에 데이터 디스크를 설정 하 여 읽기 전용 호스트 캐싱을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="7fde7-115">이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="7fde7-116">예제 2: 가상 컴퓨터의 모든 데이터 디스크에 대 한 호스트 캐싱 수정</span><span class="sxs-lookup"><span data-stu-id="7fde7-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="7fde7-117">이 명령은 ContosoService 클라우드 서비스의 VirtualMachine07 이라는 가상 컴퓨터에 대 한 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="7fde7-118">명령이 해당 가상 컴퓨터에 대 한 데이터 디스크를 가져오는 **AzureDataDisk** cmdlet에이를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="7fde7-119">그런 다음 현재 cmdlet은 각 데이터 디스크의 호스트 캐싱 모드를 ReadWrite로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="7fde7-120">이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="7fde7-121">변수</span><span class="sxs-lookup"><span data-stu-id="7fde7-121">PARAMETERS</span></span>

### <span data-ttu-id="7fde7-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7fde7-122">-DiskName</span></span>
<span data-ttu-id="7fde7-123">이 cmdlet이 수정 하는 데이터 디스크 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fde7-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="7fde7-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="7fde7-125">디스크 캐시는 4 TiB 이상에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="7fde7-126">VM에 여러 개의 디스크가 연결 된 경우 4 TiB 보다 작은 각 디스크는 캐싱을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="7fde7-127">Azure 디스크의 캐시 설정을 변경 하면 대상 디스크가 분리 되 고 다시 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="7fde7-128">운영 체제 디스크인 경우 VM이 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="7fde7-129">디스크 캐시 설정을 변경 하기 전에이 중단에 영향을 받을 수 있는 모든 응용 프로그램/서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="7fde7-130">이러한 권장 사항을 팔 로우 하지 않으면 데이터 손상이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="7fde7-131">디스크의 호스트 수준 캐싱 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="7fde7-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-132">Valid values are:</span></span>

- <span data-ttu-id="7fde7-133">않아야</span><span class="sxs-lookup"><span data-stu-id="7fde7-133">None</span></span>
- <span data-ttu-id="7fde7-134">읽기</span><span class="sxs-lookup"><span data-stu-id="7fde7-134">ReadOnly</span></span>
- <span data-ttu-id="7fde7-135">쓰기</span><span class="sxs-lookup"><span data-stu-id="7fde7-135">ReadWrite</span></span>

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

### <span data-ttu-id="7fde7-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7fde7-136">-InformationAction</span></span>
<span data-ttu-id="7fde7-137">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7fde7-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7fde7-139">하기로</span><span class="sxs-lookup"><span data-stu-id="7fde7-139">Continue</span></span>
- <span data-ttu-id="7fde7-140">숨기기</span><span class="sxs-lookup"><span data-stu-id="7fde7-140">Ignore</span></span>
- <span data-ttu-id="7fde7-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="7fde7-141">Inquire</span></span>
- <span data-ttu-id="7fde7-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7fde7-142">SilentlyContinue</span></span>
- <span data-ttu-id="7fde7-143">중지가</span><span class="sxs-lookup"><span data-stu-id="7fde7-143">Stop</span></span>
- <span data-ttu-id="7fde7-144">대기</span><span class="sxs-lookup"><span data-stu-id="7fde7-144">Suspend</span></span>

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

### <span data-ttu-id="7fde7-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7fde7-145">-InformationVariable</span></span>
<span data-ttu-id="7fde7-146">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7fde7-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="7fde7-147">-LUN</span></span>
<span data-ttu-id="7fde7-148">가상 컴퓨터의 데이터 드라이브에 대 한 LUN을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="7fde7-149">유효한 값은 0 ~ 15입니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fde7-150">-프로필</span><span class="sxs-lookup"><span data-stu-id="7fde7-150">-Profile</span></span>
<span data-ttu-id="7fde7-151">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7fde7-152">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7fde7-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7fde7-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="7fde7-154">데이터 디스크의 새 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="7fde7-155">새 크기는 현재 크기 보다 커야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fde7-156">-VM</span><span class="sxs-lookup"><span data-stu-id="7fde7-156">-VM</span></span>
<span data-ttu-id="7fde7-157">데이터 디스크에 연결 된 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="7fde7-158">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="7fde7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fde7-159">CommonParameters</span></span>
<span data-ttu-id="7fde7-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fde7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fde7-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fde7-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fde7-162">입력</span><span class="sxs-lookup"><span data-stu-id="7fde7-162">INPUTS</span></span>

## <span data-ttu-id="7fde7-163">출력</span><span class="sxs-lookup"><span data-stu-id="7fde7-163">OUTPUTS</span></span>

## <span data-ttu-id="7fde7-164">상속자</span><span class="sxs-lookup"><span data-stu-id="7fde7-164">NOTES</span></span>

## <span data-ttu-id="7fde7-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fde7-165">RELATED LINKS</span></span>

[<span data-ttu-id="7fde7-166">-AzureDataDisk 추가</span><span class="sxs-lookup"><span data-stu-id="7fde7-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="7fde7-167">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7fde7-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7fde7-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7fde7-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="7fde7-169">-AzureDataDisk 제거</span><span class="sxs-lookup"><span data-stu-id="7fde7-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="7fde7-170">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7fde7-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


