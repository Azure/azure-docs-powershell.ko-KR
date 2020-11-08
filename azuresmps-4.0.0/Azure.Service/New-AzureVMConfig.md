---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046197"
---
# <span data-ttu-id="b77d2-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b77d2-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="b77d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b77d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b77d2-103">Azure 가상 컴퓨터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="b77d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b77d2-104">SYNTAX</span></span>

### <span data-ttu-id="b77d2-105">ImageName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b77d2-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b77d2-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="b77d2-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b77d2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b77d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b77d2-108">**AzureVMConfig** Cmdlet은 Azure 가상 컴퓨터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="b77d2-109">이 개체를 사용 하 여 새 배포를 수행 하 고 기존 배포에 새 가상 컴퓨터를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="b77d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b77d2-110">EXAMPLES</span></span>

### <span data-ttu-id="b77d2-111">예제 1: Windows 가상 컴퓨터 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="b77d2-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="b77d2-112">이 명령은 운영 체제 디스크, 데이터 디스크 및 프로비저닝 구성을 사용 하 여 Windows 가상 컴퓨터 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="b77d2-113">그런 다음이 구성을 사용 하 여 새 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="b77d2-114">예제 2: Linux 가상 컴퓨터 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="b77d2-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="b77d2-115">이 명령은 운영 체제 디스크, 데이터 디스크 및 프로비저닝 구성을 사용 하 여 새 Linux 가상 컴퓨터 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="b77d2-116">그런 다음이 구성을 사용 하 여 새 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="b77d2-117">변수</span><span class="sxs-lookup"><span data-stu-id="b77d2-117">PARAMETERS</span></span>

### <span data-ttu-id="b77d2-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b77d2-118">-AvailabilitySetName</span></span>
<span data-ttu-id="b77d2-119">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b77d2-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="b77d2-121">구성을 통해 부팅 진단이 해제 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="b77d2-122">기본적으로 가상 머신에서 부팅 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="b77d2-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="b77d2-123">-DiskLabel</span></span>
<span data-ttu-id="b77d2-124">운영 체제 디스크에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b77d2-125">-DiskName</span></span>
<span data-ttu-id="b77d2-126">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="b77d2-127">-HostCaching</span></span>
<span data-ttu-id="b77d2-128">운영 체제 디스크에 대 한 호스트 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="b77d2-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-129">Valid values are:</span></span>

- <span data-ttu-id="b77d2-130">읽기</span><span class="sxs-lookup"><span data-stu-id="b77d2-130">ReadOnly</span></span>
- <span data-ttu-id="b77d2-131">쓰기</span><span class="sxs-lookup"><span data-stu-id="b77d2-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b77d2-132">-ImageName</span></span>
<span data-ttu-id="b77d2-133">운영 체제 디스크에 사용할 가상 컴퓨터 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b77d2-134">-InformationAction</span></span>
<span data-ttu-id="b77d2-135">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b77d2-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b77d2-137">하기로</span><span class="sxs-lookup"><span data-stu-id="b77d2-137">Continue</span></span>
- <span data-ttu-id="b77d2-138">숨기기</span><span class="sxs-lookup"><span data-stu-id="b77d2-138">Ignore</span></span>
- <span data-ttu-id="b77d2-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="b77d2-139">Inquire</span></span>
- <span data-ttu-id="b77d2-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b77d2-140">SilentlyContinue</span></span>
- <span data-ttu-id="b77d2-141">중지가</span><span class="sxs-lookup"><span data-stu-id="b77d2-141">Stop</span></span>
- <span data-ttu-id="b77d2-142">대기</span><span class="sxs-lookup"><span data-stu-id="b77d2-142">Suspend</span></span>

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

### <span data-ttu-id="b77d2-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b77d2-143">-InformationVariable</span></span>
<span data-ttu-id="b77d2-144">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b77d2-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="b77d2-145">-InstanceSize</span></span>
<span data-ttu-id="b77d2-146">인스턴스의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="b77d2-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b77d2-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="b77d2-148">ExtraSmall</span></span>
- <span data-ttu-id="b77d2-149">Small</span><span class="sxs-lookup"><span data-stu-id="b77d2-149">Small</span></span>
- <span data-ttu-id="b77d2-150">높음이나</span><span class="sxs-lookup"><span data-stu-id="b77d2-150">Medium</span></span>
- <span data-ttu-id="b77d2-151">용량의</span><span class="sxs-lookup"><span data-stu-id="b77d2-151">Large</span></span>
- <span data-ttu-id="b77d2-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="b77d2-152">ExtraLarge</span></span>
- <span data-ttu-id="b77d2-153">5</span><span class="sxs-lookup"><span data-stu-id="b77d2-153">A5</span></span>
- <span data-ttu-id="b77d2-154">A6</span><span class="sxs-lookup"><span data-stu-id="b77d2-154">A6</span></span>
- <span data-ttu-id="b77d2-155">(A</span><span class="sxs-lookup"><span data-stu-id="b77d2-155">A7</span></span>
- <span data-ttu-id="b77d2-156">A8</span><span class="sxs-lookup"><span data-stu-id="b77d2-156">A8</span></span>
- <span data-ttu-id="b77d2-157">A9</span><span class="sxs-lookup"><span data-stu-id="b77d2-157">A9</span></span>
- <span data-ttu-id="b77d2-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="b77d2-158">Basic_A0</span></span>
- <span data-ttu-id="b77d2-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="b77d2-159">Basic_A1</span></span>
- <span data-ttu-id="b77d2-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="b77d2-160">Basic_A2</span></span>
- <span data-ttu-id="b77d2-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="b77d2-161">Basic_A3</span></span>
- <span data-ttu-id="b77d2-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="b77d2-162">Basic_A4</span></span>
- <span data-ttu-id="b77d2-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="b77d2-163">Standard_D1</span></span>
- <span data-ttu-id="b77d2-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="b77d2-164">Standard_D2</span></span>
- <span data-ttu-id="b77d2-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="b77d2-165">Standard_D3</span></span>
- <span data-ttu-id="b77d2-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="b77d2-166">Standard_D4</span></span>
- <span data-ttu-id="b77d2-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="b77d2-167">Standard_D11</span></span>
- <span data-ttu-id="b77d2-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="b77d2-168">Standard_D12</span></span>
- <span data-ttu-id="b77d2-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="b77d2-169">Standard_D13</span></span>
- <span data-ttu-id="b77d2-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="b77d2-170">Standard_D14</span></span>

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

### <span data-ttu-id="b77d2-171">-레이블</span><span class="sxs-lookup"><span data-stu-id="b77d2-171">-Label</span></span>
<span data-ttu-id="b77d2-172">가상 컴퓨터에 할당할 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b77d2-173">-LicenseType</span></span>
<span data-ttu-id="b77d2-174">온-프레미스 라이선스가 있는 이미지나 디스크에 대 한 라이선스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="b77d2-175">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b77d2-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b77d2-176">Windows_Client</span></span>
- <span data-ttu-id="b77d2-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="b77d2-177">Windows_Server</span></span> 

<span data-ttu-id="b77d2-178">Windows Server 운영 체제를 포함 하는 이미지에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="b77d2-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="b77d2-179">-MediaLocation</span></span>
<span data-ttu-id="b77d2-180">새 가상 컴퓨터 디스크에 대 한 Azure 저장소 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d2-181">-이름</span><span class="sxs-lookup"><span data-stu-id="b77d2-181">-Name</span></span>
<span data-ttu-id="b77d2-182">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b77d2-183">-프로필</span><span class="sxs-lookup"><span data-stu-id="b77d2-183">-Profile</span></span>
<span data-ttu-id="b77d2-184">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b77d2-185">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b77d2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77d2-186">CommonParameters</span></span>
<span data-ttu-id="b77d2-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b77d2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77d2-188">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77d2-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77d2-189">입력</span><span class="sxs-lookup"><span data-stu-id="b77d2-189">INPUTS</span></span>

## <span data-ttu-id="b77d2-190">출력</span><span class="sxs-lookup"><span data-stu-id="b77d2-190">OUTPUTS</span></span>

## <span data-ttu-id="b77d2-191">상속자</span><span class="sxs-lookup"><span data-stu-id="b77d2-191">NOTES</span></span>

## <span data-ttu-id="b77d2-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b77d2-192">RELATED LINKS</span></span>

