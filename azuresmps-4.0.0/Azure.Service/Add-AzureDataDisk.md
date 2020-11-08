---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045735"
---
# <span data-ttu-id="c608a-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c608a-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="c608a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c608a-102">SYNOPSIS</span></span>
<span data-ttu-id="c608a-103">가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="c608a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c608a-104">SYNTAX</span></span>

### <span data-ttu-id="c608a-105">CreateNew (기본값)</span><span class="sxs-lookup"><span data-stu-id="c608a-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c608a-106">Import</span><span class="sxs-lookup"><span data-stu-id="c608a-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c608a-107">가져오기 원본</span><span class="sxs-lookup"><span data-stu-id="c608a-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c608a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c608a-108">DESCRIPTION</span></span>
<span data-ttu-id="c608a-109">**추가-AzureDataDisk** cmdlet은 새 또는 기존 데이터 디스크를 Azure 가상 컴퓨터 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="c608a-110">*CreateNew* 매개 변수를 사용 하 여 지정 된 크기 및 레이블을 갖는 새 데이터 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="c608a-111">*Import* 매개 변수를 사용 하 여 이미지 리포지토리의 기존 디스크를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="c608a-112">*가져오기* 매개 변수를 사용 하 여 저장소 계정의 blob에서 기존 디스크를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="c608a-113">연결 된 데이터 디스크의 호스트 캐시 모드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="c608a-114">예제의</span><span class="sxs-lookup"><span data-stu-id="c608a-114">EXAMPLES</span></span>

### <span data-ttu-id="c608a-115">예제 1: 리포지토리에서 데이터 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="c608a-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c608a-116">이 명령은 **VirtualMachine07 cmdlet을** 사용 하 여 ContosoService cloud 서비스의 가상 컴퓨터 이름에 대 한 가상 컴퓨터 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c608a-117">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c608a-118">이 명령은 저장소의 기존 데이터 디스크를 가상 컴퓨터에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="c608a-119">데이터 디스크의 LUN은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="c608a-120">이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="c608a-121">예제 2: 새 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="c608a-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c608a-122">이 명령은 VirtualMachine08 이라는 가상 컴퓨터에 대 한 가상 컴퓨터 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="c608a-123">명령이 현재 cmdlet에이를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="c608a-124">이 명령은 MyNewDisk 이라는 새 데이터 디스크를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="c608a-125">Cmdlet은 현재 구독에 대 한 기본 저장소 계정의 vhd 컨테이너에 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="c608a-126">이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="c608a-127">예제 3: 지정 된 위치에서 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="c608a-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c608a-128">이 명령은 가상 머신 데이터베이스에 대 한 가상 머신 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="c608a-129">명령이 현재 cmdlet에이를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="c608a-130">이 명령은 지정 된 위치에서 Disk14 라는 기존 데이터 디스크를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="c608a-131">이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="c608a-132">변수</span><span class="sxs-lookup"><span data-stu-id="c608a-132">PARAMETERS</span></span>

### <span data-ttu-id="c608a-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="c608a-133">-CreateNew</span></span>
<span data-ttu-id="c608a-134">이 cmdlet이 데이터 디스크를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="c608a-135">-DiskLabel</span></span>
<span data-ttu-id="c608a-136">새 데이터 디스크에 대 한 디스크 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c608a-137">-DiskName</span></span>
<span data-ttu-id="c608a-138">디스크 리포지토리의 데이터 디스크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c608a-139">-DiskSizeInGB</span></span>
<span data-ttu-id="c608a-140">새 데이터 디스크에 대 한 논리 디스크 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="c608a-141">-HostCaching</span></span>
<span data-ttu-id="c608a-142">디스크의 호스트 수준 캐싱 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="c608a-143">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-143">Valid values are:</span></span> 

- <span data-ttu-id="c608a-144">않아야</span><span class="sxs-lookup"><span data-stu-id="c608a-144">None</span></span> 
- <span data-ttu-id="c608a-145">읽기</span><span class="sxs-lookup"><span data-stu-id="c608a-145">ReadOnly</span></span> 
- <span data-ttu-id="c608a-146">쓰기</span><span class="sxs-lookup"><span data-stu-id="c608a-146">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-147">-가져오기</span><span class="sxs-lookup"><span data-stu-id="c608a-147">-Import</span></span>
<span data-ttu-id="c608a-148">이 cmdlet이 이미지 리포지토리에서 기존 데이터 디스크를 가져오도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="c608a-149">-ImportFrom</span></span>
<span data-ttu-id="c608a-150">이 cmdlet이 저장소 계정의 blob에서 기존 데이터 디스크를 가져오도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c608a-151">-InformationAction</span></span>
<span data-ttu-id="c608a-152">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c608a-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c608a-154">하기로</span><span class="sxs-lookup"><span data-stu-id="c608a-154">Continue</span></span>
- <span data-ttu-id="c608a-155">숨기기</span><span class="sxs-lookup"><span data-stu-id="c608a-155">Ignore</span></span>
- <span data-ttu-id="c608a-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="c608a-156">Inquire</span></span>
- <span data-ttu-id="c608a-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c608a-157">SilentlyContinue</span></span>
- <span data-ttu-id="c608a-158">중지가</span><span class="sxs-lookup"><span data-stu-id="c608a-158">Stop</span></span>
- <span data-ttu-id="c608a-159">대기</span><span class="sxs-lookup"><span data-stu-id="c608a-159">Suspend</span></span>

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

### <span data-ttu-id="c608a-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c608a-160">-InformationVariable</span></span>
<span data-ttu-id="c608a-161">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c608a-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="c608a-162">-LUN</span></span>
<span data-ttu-id="c608a-163">가상 컴퓨터의 데이터 드라이브에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="c608a-164">유효한 값은 0 ~ 15입니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="c608a-165">각 데이터 디스크에는 고유한 LUN이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="c608a-166">-MediaLocation</span></span>
<span data-ttu-id="c608a-167">이 cmdlet이 데이터 디스크를 저장 하는 Azure storage 계정에서 blob의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="c608a-168">위치를 지정 하지 않으면 cmdlet은 현재 구독에 대 한 기본 저장소 계정의 데이터 디스크를 vhd 컨테이너에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="c608a-169">Vhd 컨테이너가 없는 경우 cmdlet은 vhd 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c608a-170">-프로필</span><span class="sxs-lookup"><span data-stu-id="c608a-170">-Profile</span></span>
<span data-ttu-id="c608a-171">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c608a-172">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c608a-173">-VM</span><span class="sxs-lookup"><span data-stu-id="c608a-173">-VM</span></span>
<span data-ttu-id="c608a-174">이 cmdlet이 데이터 디스크를 연결 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="c608a-175">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="c608a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c608a-176">CommonParameters</span></span>
<span data-ttu-id="c608a-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c608a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c608a-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c608a-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c608a-179">입력</span><span class="sxs-lookup"><span data-stu-id="c608a-179">INPUTS</span></span>

## <span data-ttu-id="c608a-180">출력</span><span class="sxs-lookup"><span data-stu-id="c608a-180">OUTPUTS</span></span>

## <span data-ttu-id="c608a-181">상속자</span><span class="sxs-lookup"><span data-stu-id="c608a-181">NOTES</span></span>

## <span data-ttu-id="c608a-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c608a-182">RELATED LINKS</span></span>

[<span data-ttu-id="c608a-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c608a-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="c608a-184">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="c608a-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c608a-185">-AzureDataDisk 제거</span><span class="sxs-lookup"><span data-stu-id="c608a-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="c608a-186">Set AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c608a-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="c608a-187">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="c608a-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


