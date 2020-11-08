---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045517"
---
# <span data-ttu-id="8068c-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8068c-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="8068c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8068c-102">SYNOPSIS</span></span>
<span data-ttu-id="8068c-103">인라인 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="8068c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8068c-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8068c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8068c-105">DESCRIPTION</span></span>
<span data-ttu-id="8068c-106">**AzureStorSimpleInlineStorageAccountCredential** cmdlet은 인라인 Azure storage 계정 자격 증명 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="8068c-107">이 cmdlet은 더미 자격 증명 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="8068c-108">Windows PowerShell 파이프라인을 사용 하 여 동일한 명령에서 **AzureStorSimpleDeviceVolumeContainer** cmdlet 및 현재 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="8068c-109">실제 저장소 계정 자격 증명 개체는 볼륨 컨테이너 만들기의 일부로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="8068c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8068c-110">EXAMPLES</span></span>

### <span data-ttu-id="8068c-111">예제 1: 저장소 계정 자격 증명 인라인 만들기</span><span class="sxs-lookup"><span data-stu-id="8068c-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="8068c-112">이 명령은 저장소 계정 자격 증명을 인라인으로 만든 다음 파이프라인 연산자를 사용 하 여 **새 AzureStorSimpleDeviceVolumeContainer** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8068c-113">해당 컨테이너는 더미 자격 증명을 사용 하 여 볼륨 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="8068c-114">변수</span><span class="sxs-lookup"><span data-stu-id="8068c-114">PARAMETERS</span></span>

### <span data-ttu-id="8068c-115">-끝점</span><span class="sxs-lookup"><span data-stu-id="8068c-115">-Endpoint</span></span>
<span data-ttu-id="8068c-116">저장소 계정에 대 한 Azure 저장소 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="8068c-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="8068c-117">-Profile</span></span>
<span data-ttu-id="8068c-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8068c-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8068c-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8068c-120">-StorageAccountKey</span></span>
<span data-ttu-id="8068c-121">저장소 계정의 계정 키를 일반 텍스트로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="8068c-122">키가 암호화 된 형식으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068c-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8068c-123">-StorageAccountName</span></span>
<span data-ttu-id="8068c-124">기존 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-124">Specifies the name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8068c-125">CommonParameters</span></span>
<span data-ttu-id="8068c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8068c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8068c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8068c-128">입력</span><span class="sxs-lookup"><span data-stu-id="8068c-128">INPUTS</span></span>

### <span data-ttu-id="8068c-129">않아야</span><span class="sxs-lookup"><span data-stu-id="8068c-129">None</span></span>

## <span data-ttu-id="8068c-130">출력</span><span class="sxs-lookup"><span data-stu-id="8068c-130">OUTPUTS</span></span>

### <span data-ttu-id="8068c-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="8068c-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="8068c-132">이 cmdlet은 다음 필드가 포함 된 **Cloudtype** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="8068c-133">**호스트 이름**.</span><span class="sxs-lookup"><span data-stu-id="8068c-133">**Hostname**.</span></span>
<span data-ttu-id="8068c-134">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-134">**String**.</span></span> 
- <span data-ttu-id="8068c-135">**InstanceId**.</span><span class="sxs-lookup"><span data-stu-id="8068c-135">**InstanceId**.</span></span>
<span data-ttu-id="8068c-136">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-136">**String**.</span></span> 
- <span data-ttu-id="8068c-137">**IsDefault**.</span><span class="sxs-lookup"><span data-stu-id="8068c-137">**IsDefault**.</span></span>
<span data-ttu-id="8068c-138">**부울** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-138">**Boolean**.</span></span> 
- <span data-ttu-id="8068c-139">**위치**.</span><span class="sxs-lookup"><span data-stu-id="8068c-139">**Location**.</span></span>
<span data-ttu-id="8068c-140">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-140">**String**.</span></span> 
- <span data-ttu-id="8068c-141">**로그인** 합니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-141">**Login**.</span></span>
<span data-ttu-id="8068c-142">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-142">**String**.</span></span> 
- <span data-ttu-id="8068c-143">**이름** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-143">**Name**.</span></span>
<span data-ttu-id="8068c-144">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-144">**String**.</span></span> 
- <span data-ttu-id="8068c-145">**Operationinprogress**.</span><span class="sxs-lookup"><span data-stu-id="8068c-145">**OperationInProgress**.</span></span>
<span data-ttu-id="8068c-146">**Operationinprogress**.</span><span class="sxs-lookup"><span data-stu-id="8068c-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="8068c-147">**비밀 번호**.</span><span class="sxs-lookup"><span data-stu-id="8068c-147">**Password**.</span></span>
<span data-ttu-id="8068c-148">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-148">**String**.</span></span> 
- <span data-ttu-id="8068c-149">**Password\ Certthumbprint**.</span><span class="sxs-lookup"><span data-stu-id="8068c-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="8068c-150">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-150">**String**.</span></span> 
- <span data-ttu-id="8068c-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="8068c-151">**UseSSL**.</span></span>
<span data-ttu-id="8068c-152">**부울** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-152">**Boolean**.</span></span> 
- <span data-ttu-id="8068c-153">(고) **ecount**.</span><span class="sxs-lookup"><span data-stu-id="8068c-153">**VolumeCount**.</span></span>
<span data-ttu-id="8068c-154">**정수** 입니다.</span><span class="sxs-lookup"><span data-stu-id="8068c-154">**Integer**.</span></span>

## <span data-ttu-id="8068c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="8068c-155">NOTES</span></span>

## <span data-ttu-id="8068c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8068c-156">RELATED LINKS</span></span>

[<span data-ttu-id="8068c-157">새-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8068c-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8068c-158">새로운 AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8068c-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


