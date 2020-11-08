---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045520"
---
# <span data-ttu-id="042e6-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="042e6-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="042e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="042e6-102">SYNOPSIS</span></span>
<span data-ttu-id="042e6-103">볼륨 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-103">Creates a volume container.</span></span>

## <span data-ttu-id="042e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="042e6-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="042e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="042e6-105">DESCRIPTION</span></span>
<span data-ttu-id="042e6-106">**새 AzureStorSimpleDeviceVolumeContainer** cmdlet은 볼륨 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="042e6-107">저장소 계정 자격 증명을 새 볼륨 컨테이너에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="042e6-108">저장소 계정 자격 증명을 얻으려면 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="042e6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="042e6-109">EXAMPLES</span></span>

### <span data-ttu-id="042e6-110">예제 1: 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="042e6-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="042e6-111">이 명령은 **Get-Azurestorsimplestoragecredential** cmdlet을 사용 하 여 ContosoAccount 이라는 계정에 대 한 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="042e6-112">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 자격 증명을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="042e6-113">이 cmdlet은 해당 cmdlet의 자격 증명을 사용 하 여 Contoso63-AppVm 이라는 장치에서 Container08 이라는 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="042e6-114">이 명령은 작업을 시작한 다음 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="042e6-115">작업 상태를 확인 하려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="042e6-116">변수</span><span class="sxs-lookup"><span data-stu-id="042e6-116">PARAMETERS</span></span>

### <span data-ttu-id="042e6-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="042e6-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="042e6-118">대역폭 속도를 초당 메가 비트 (Mbps)로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042e6-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="042e6-119">-DeviceName</span></span>
<span data-ttu-id="042e6-120">볼륨 컨테이너를 만들 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042e6-121">-# 사용</span><span class="sxs-lookup"><span data-stu-id="042e6-121">-EncryptionEnabled</span></span>
<span data-ttu-id="042e6-122">암호화를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-122">Indicates whether to enable encryption.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042e6-123">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="042e6-123">-EncryptionKey</span></span>
<span data-ttu-id="042e6-124">암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="042e6-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="042e6-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="042e6-126">새 볼륨 컨테이너에 연결할 자격 증명을 **Storageaccountcredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="042e6-127">**Storageaccountcredential** 개체를 가져오려면 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="042e6-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="042e6-128">-Profile</span></span>
<span data-ttu-id="042e6-129">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="042e6-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="042e6-130">-VolumeContainerName</span></span>
<span data-ttu-id="042e6-131">만들 볼륨 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-131">Specifies the name of the volume container to create.</span></span>

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

### <span data-ttu-id="042e6-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="042e6-132">-WaitForComplete</span></span>
<span data-ttu-id="042e6-133">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="042e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042e6-134">CommonParameters</span></span>
<span data-ttu-id="042e6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042e6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042e6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042e6-137">입력</span><span class="sxs-lookup"><span data-stu-id="042e6-137">INPUTS</span></span>

### <span data-ttu-id="042e6-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="042e6-138">StorageAccountCredential</span></span>
<span data-ttu-id="042e6-139">이 cmdlet은 볼륨 컨테이너에 연결 하는 **Primarystorageaccountcredential** 개체를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="042e6-140">출력</span><span class="sxs-lookup"><span data-stu-id="042e6-140">OUTPUTS</span></span>

### <span data-ttu-id="042e6-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="042e6-141">TaskStatusInfo</span></span>
<span data-ttu-id="042e6-142">*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="042e6-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="042e6-143">상속자</span><span class="sxs-lookup"><span data-stu-id="042e6-143">NOTES</span></span>

## <span data-ttu-id="042e6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="042e6-144">RELATED LINKS</span></span>

[<span data-ttu-id="042e6-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="042e6-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="042e6-146">제거-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="042e6-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="042e6-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="042e6-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="042e6-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="042e6-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


