---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045513"
---
# <span data-ttu-id="f094c-101">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f094c-101">New-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="f094c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f094c-102">SYNOPSIS</span></span>
<span data-ttu-id="f094c-103">Azure 저장소 액세스 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-103">Adds an Azure storage access credential.</span></span>

## <span data-ttu-id="f094c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f094c-104">SYNTAX</span></span>

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f094c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f094c-105">DESCRIPTION</span></span>
<span data-ttu-id="f094c-106">**새-AzureStorSimpleStorageAccountCredential** Cmdlet은 storsimple OneSDK cmdlet에서 사용할 수 있도록 storsimple Manager에 Azure 저장소 액세스 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-106">The **New-AzureStorSimpleStorageAccountCredential** cmdlet adds an Azure storage access credential to StorSimple manager for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="f094c-107">대부분의 StorSimple OneSDK cmdlet은 볼륨, 볼륨 컨테이너, 백업, 백업 정책 등의 특정 저장소 계정에 연결 되는 엔터티를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-107">Most of the StorSimple OneSDK cmdlets deal with entities that are eventually tied to a specific storage account, such as volumes, volume containers, backups, and backup policies.</span></span>
<span data-ttu-id="f094c-108">일부 cmdlet의 경우 사용 중인 저장소 계정의 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-108">For some cmdlets, you must provide the credentials of the storage account in use.</span></span>
<span data-ttu-id="f094c-109">저장소 계정 자격 증명은 OneSDK에서 만든 access 개체 이며,이는 기존 Azure 저장소 계정을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-109">A storage account credential is an access object created in OneSDK that points to an existing Azure storage account.</span></span>
<span data-ttu-id="f094c-110">저장소 계정 자격 증명을 만들기 위해 기존 저장소 계정의 이름 및 선택 키를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-110">You provide the name and access key of an existing storage account to create a storage account credential.</span></span>
<span data-ttu-id="f094c-111">그런 다음 다른 cmdlet에 해당 자격 증명 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-111">You can then use that credential object with other cmdlets.</span></span>

<span data-ttu-id="f094c-112">이 cmdlet은 **-Azurestorsimplerazurecmdlet** 을 사용 하 여 리소스를 선택할 때 제공 하는 등록 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-112">This cmdlet uses the registration key that you provide when you select the resource by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>
<span data-ttu-id="f094c-113">암호화 오류를 방지 하기 위해 값이 정확한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-113">Be sure that value is correct to avoid encryption failure.</span></span>
<span data-ttu-id="f094c-114">등록 키를 올바른 값으로 수정 하려면, **선택-AzureStorSimpleResource** 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-114">To modify the registration key to a correct value, use **Select-AzureStorSimpleResource**.</span></span>

## <span data-ttu-id="f094c-115">예제의</span><span class="sxs-lookup"><span data-stu-id="f094c-115">EXAMPLES</span></span>

### <span data-ttu-id="f094c-116">예제 1: 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="f094c-116">Example 1: Create a credential</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="f094c-117">이 명령은 지정 된 저장소 계정에 대 한 저장소 액세스 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-117">This command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="f094c-118">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로, cmdlet은 작업이 완료 될 때까지 대기 하 여 콘솔에 제어를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-118">This command specifies the *WaitForComplete* parameter, and, so, the cmdlet waits until the task finishes to return control to the console.</span></span>

### <span data-ttu-id="f094c-119">예제 2: 자격 증명 만들기 및 작업 상태 쿼리</span><span class="sxs-lookup"><span data-stu-id="f094c-119">Example 2: Create a credential and query that status of the task</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

<span data-ttu-id="f094c-120">첫 번째 명령은 지정 된 저장소 계정에 대 한 저장소 액세스 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-120">The first command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="f094c-121">이 명령은 작업 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-121">The command returns a task ID.</span></span>

<span data-ttu-id="f094c-122">두 번째 명령은 **Get-AzureStorSimpleTask** cmdlet을 사용 하 여 작업의 상태를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-122">The second command queries the status of the task by using the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="f094c-123">명령은 첫 번째 명령의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-123">The command specifies the task ID from the first command.</span></span>

### <span data-ttu-id="f094c-124">예제 3: 다른 cmdlet에 사용할 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="f094c-124">Example 3: Create a credential to use with another cmdlet</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="f094c-125">이 명령은 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-125">This command creates a storage account credential.</span></span>
<span data-ttu-id="f094c-126">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 **AzureStorSimpleDeviceVolumeContainer** cmdlet에 해당 자격 증명을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-126">The command then passes that credential to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f094c-127">해당 cmdlet은 자격 증명을 사용 하 여 새 볼륨 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-127">That cmdlet creates a new volume container by using the credential.</span></span>

## <span data-ttu-id="f094c-128">변수</span><span class="sxs-lookup"><span data-stu-id="f094c-128">PARAMETERS</span></span>

### <span data-ttu-id="f094c-129">-끝점</span><span class="sxs-lookup"><span data-stu-id="f094c-129">-Endpoint</span></span>
<span data-ttu-id="f094c-130">저장소 계정에 대 한 Azure 저장소 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-130">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="f094c-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="f094c-131">-Profile</span></span>
<span data-ttu-id="f094c-132">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f094c-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f094c-133">-StorageAccountKey</span></span>
<span data-ttu-id="f094c-134">일반 텍스트로 저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-134">Specifies the access key of the storage account in plain text.</span></span>

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

### <span data-ttu-id="f094c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f094c-135">-StorageAccountName</span></span>
<span data-ttu-id="f094c-136">기존 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-136">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="f094c-137">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="f094c-137">-UseSSL</span></span>
<span data-ttu-id="f094c-138">새 저장소 계정 자격 증명을 사용 하는 경우 연결에 SSL을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-138">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f094c-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f094c-139">-WaitForComplete</span></span>
<span data-ttu-id="f094c-140">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f094c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f094c-141">CommonParameters</span></span>
<span data-ttu-id="f094c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f094c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f094c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f094c-144">입력</span><span class="sxs-lookup"><span data-stu-id="f094c-144">INPUTS</span></span>

### <span data-ttu-id="f094c-145">않아야</span><span class="sxs-lookup"><span data-stu-id="f094c-145">None</span></span>

## <span data-ttu-id="f094c-146">출력</span><span class="sxs-lookup"><span data-stu-id="f094c-146">OUTPUTS</span></span>

### <span data-ttu-id="f094c-147">IEnumerable \<StorageAccountCredentialResponse\> , taskresponse</span><span class="sxs-lookup"><span data-stu-id="f094c-147">IEnumerable\<StorageAccountCredentialResponse\>, TaskResponse</span></span>
<span data-ttu-id="f094c-148">이 cmdlet은 *Waitforcomplete* 매개 변수를 지정 하는 경우 **Storageaccountcredentialresponse** 개체의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-148">This cmdlet returns a list of **StorageAccountCredentialResponse** objects, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="f094c-149">이 매개 변수를 지정 하지 않으면 cmdlet이 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-149">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="f094c-150">**Storageaccountcredentialresponse** 에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f094c-150">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="f094c-151">**Cloudtype** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="f094c-151">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="f094c-152">**호스트 이름** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f094c-152">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="f094c-153">**InstanceId** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f094c-153">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="f094c-154">**IsDefault** ( **부울** )</span><span class="sxs-lookup"><span data-stu-id="f094c-154">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="f094c-155">**위치** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="f094c-155">**Location** ( **String** )</span></span>
- <span data-ttu-id="f094c-156">**로그인** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="f094c-156">**Login** ( **String** )</span></span>
- <span data-ttu-id="f094c-157">**Name** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f094c-157">**Name** ( **String** )</span></span>
- <span data-ttu-id="f094c-158">**Operationinprogress** ( **operationinprogress** )</span><span class="sxs-lookup"><span data-stu-id="f094c-158">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="f094c-159">**암호** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="f094c-159">**Password** ( **String** )</span></span>
- <span data-ttu-id="f094c-160">**Password. Cert손도장** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f094c-160">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="f094c-161">**UseSSL** ( **부울** )</span><span class="sxs-lookup"><span data-stu-id="f094c-161">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="f094c-162">**(** **Int** ).</span><span class="sxs-lookup"><span data-stu-id="f094c-162">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="f094c-163">상속자</span><span class="sxs-lookup"><span data-stu-id="f094c-163">NOTES</span></span>

## <span data-ttu-id="f094c-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f094c-164">RELATED LINKS</span></span>

[<span data-ttu-id="f094c-165">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f094c-165">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="f094c-166">-AzureStorSimpleStorageAccountCredential 제거</span><span class="sxs-lookup"><span data-stu-id="f094c-166">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="f094c-167">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f094c-167">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="f094c-168">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f094c-168">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="f094c-169">새로운 AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="f094c-169">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


