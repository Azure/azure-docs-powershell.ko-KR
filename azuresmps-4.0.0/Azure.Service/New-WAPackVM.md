---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047398"
---
# <span data-ttu-id="71faa-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-101">New-WAPackVM</span></span>

## <span data-ttu-id="71faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71faa-102">SYNOPSIS</span></span>
<span data-ttu-id="71faa-103">가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="71faa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71faa-104">SYNTAX</span></span>

### <span data-ttu-id="71faa-105">CreateVMFromTemplate (기본값)</span><span class="sxs-lookup"><span data-stu-id="71faa-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="71faa-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="71faa-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="71faa-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="71faa-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71faa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="71faa-108">DESCRIPTION</span></span>
<span data-ttu-id="71faa-109">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="71faa-110">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="71faa-111">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="71faa-112">**새-WAPackVM** cmdlet은 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="71faa-113">예제의</span><span class="sxs-lookup"><span data-stu-id="71faa-113">EXAMPLES</span></span>

### <span data-ttu-id="71faa-114">예제 1: 템플릿을 사용 하 여 Windows 운영 체제의 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="71faa-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="71faa-115">첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="71faa-116">Cmdlet에서 계정과 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="71faa-117">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="71faa-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="71faa-118">두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 ContosoTemplate04 이라는 가상 컴퓨터 템플릿을 가져온 다음이를 $Template 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="71faa-119">마지막 명령은 $Template 변수에 저장 된 템플릿을 기반으로 ContosoV023 이라는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="71faa-120">명령에서 *windows* 매개 변수를 지정 하므로 가상 컴퓨터에서 windows 운영 체제 버전을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="71faa-121">예제 2: 템플릿을 사용 하 여 Linux 운영 체제에 대 한 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="71faa-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="71faa-122">첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="71faa-123">두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 ContosoTemplate19 이라는 가상 컴퓨터 템플릿을 가져온 다음이를 $Template 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="71faa-124">마지막 명령은 $Template 변수에 저장 된 템플릿을 기반으로 ContosoV028 이라는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="71faa-125">명령은 *linux* 매개 변수를 지정 하므로 가상 컴퓨터는 linux 운영 체제 버전을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="71faa-126">예제 3: 운영 체제 디스크 및 크기 프로필에서 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="71faa-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="71faa-127">첫 번째 명령은 **WAPackVMOSDisk** cmdlet을 사용 하 여 ContosoDiskOS 이라는 운영 체제 디스크를 가져온 다음이를 $OSDisk 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="71faa-128">두 번째 명령은 MediumSizeVM **Apackvmsizeprofile** cmdlet을 사용 하 여 명명 된 크기 프로필을 가져온 다음이를 $SizeProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="71faa-129">마지막 명령은 $OSDisk에 저장 된 운영 체제 디스크에서 ContosoV073 이라는 가상 컴퓨터와 $SizeProfile에 저장 된 크기 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="71faa-130">변수</span><span class="sxs-lookup"><span data-stu-id="71faa-130">PARAMETERS</span></span>

### <span data-ttu-id="71faa-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="71faa-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="71faa-132">관리자 계정에 대 한 SSH (보안 셸) 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="71faa-133">-Linux</span></span>
<span data-ttu-id="71faa-134">Cmdlet이 Linux 운영 체제를 실행 하는 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-135">-이름</span><span class="sxs-lookup"><span data-stu-id="71faa-135">-Name</span></span>
<span data-ttu-id="71faa-136">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="71faa-137">-OSDisk</span></span>
<span data-ttu-id="71faa-138">운영 체제 디스크를 **VirtualHardDisk** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="71faa-139">운영 체제 디스크를 얻으려면 **WAPackVMOSDisk** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="71faa-140">-ProductKey</span></span>
<span data-ttu-id="71faa-141">제품 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-141">Specifies a product key.</span></span>
<span data-ttu-id="71faa-142">제품 키는 제품 라이선스를 식별 하는 25 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="71faa-143">가상 컴퓨터 또는 호스트에 설치 하려는 운영 체제의 제품 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-144">-프로필</span><span class="sxs-lookup"><span data-stu-id="71faa-144">-Profile</span></span>
<span data-ttu-id="71faa-145">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71faa-146">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71faa-147">-Template</span><span class="sxs-lookup"><span data-stu-id="71faa-147">-Template</span></span>
<span data-ttu-id="71faa-148">템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-148">Specifies a template.</span></span>
<span data-ttu-id="71faa-149">Cmdlet이 지정 된 템플릿을 기반으로 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="71faa-150">템플릿 개체를 가져오려면 Get-WAPackVMTemplate cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="71faa-151">-VMCredential</span></span>
<span data-ttu-id="71faa-152">로컬 관리자 계정에 대 한 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="71faa-153">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="71faa-154">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="71faa-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="71faa-155">-VMSizeProfile</span></span>
<span data-ttu-id="71faa-156">가상 머신의 크기 프로필을 **HardwareProfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="71faa-157">크기 프로필을 얻으려면 **Get-WAPackVMSizeProfile** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="71faa-158">-VNet</span></span>
<span data-ttu-id="71faa-159">가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-159">Specifies a virtual network.</span></span>
<span data-ttu-id="71faa-160">Cmdlet이 가상 컴퓨터를 지정 된 가상 네트워크에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="71faa-161">가상 네트워크를 가져오려면 **Get-WAPackVNet** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="71faa-162">-Windows</span></span>
<span data-ttu-id="71faa-163">Cmdlet이 Windows 운영 체제를 실행 하는 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71faa-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71faa-164">CommonParameters</span></span>
<span data-ttu-id="71faa-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71faa-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71faa-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71faa-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71faa-167">입력</span><span class="sxs-lookup"><span data-stu-id="71faa-167">INPUTS</span></span>

## <span data-ttu-id="71faa-168">출력</span><span class="sxs-lookup"><span data-stu-id="71faa-168">OUTPUTS</span></span>

## <span data-ttu-id="71faa-169">상속자</span><span class="sxs-lookup"><span data-stu-id="71faa-169">NOTES</span></span>

## <span data-ttu-id="71faa-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71faa-170">RELATED LINKS</span></span>

[<span data-ttu-id="71faa-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="71faa-172">제거-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="71faa-173">다시 시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="71faa-174">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="71faa-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="71faa-176">시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="71faa-177">중지-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="71faa-178">일시 중단-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="71faa-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="71faa-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="71faa-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="71faa-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="71faa-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="71faa-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="71faa-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


