---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045851"
---
# <span data-ttu-id="bfd65-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bfd65-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="bfd65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd65-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd65-103">Azure 저장소 액세스 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="bfd65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfd65-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bfd65-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bfd65-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd65-106">**Set-AzureStorSimpleStorageAccountCredential** Cmdlet은 StorSimple OneSDK cmdlet에서 사용 하는 기존 Azure 저장소 액세스 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="bfd65-107">StorSimple cmdlet에서 저장소 계정으로 작업 하는 방법에 대 한 자세한 내용은 New-AzureStorSimpleStorageAccountCredential cmdlet에 대 한 도움말 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bfd65-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="bfd65-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bfd65-108">EXAMPLES</span></span>

### <span data-ttu-id="bfd65-109">예제 1: 자격 증명 수정</span><span class="sxs-lookup"><span data-stu-id="bfd65-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="bfd65-110">이 명령은 ContosoStorage01 이라는 저장소 계정 자격 증명을 더 이상 SSL 필요 없음으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="bfd65-111">변수</span><span class="sxs-lookup"><span data-stu-id="bfd65-111">PARAMETERS</span></span>

### <span data-ttu-id="bfd65-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="bfd65-112">-Profile</span></span>
<span data-ttu-id="bfd65-113">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bfd65-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bfd65-114">-StorageAccountKey</span></span>
<span data-ttu-id="bfd65-115">일반 텍스트로 저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd65-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bfd65-116">-StorageAccountName</span></span>
<span data-ttu-id="bfd65-117">기존 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-117">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="bfd65-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="bfd65-118">-UseSSL</span></span>
<span data-ttu-id="bfd65-119">새 저장소 계정 자격 증명을 사용 하는 경우 연결에 SSL을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

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

### <span data-ttu-id="bfd65-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="bfd65-120">-WaitForComplete</span></span>
<span data-ttu-id="bfd65-121">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="bfd65-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd65-122">CommonParameters</span></span>
<span data-ttu-id="bfd65-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd65-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd65-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd65-125">입력</span><span class="sxs-lookup"><span data-stu-id="bfd65-125">INPUTS</span></span>

### <span data-ttu-id="bfd65-126">않아야</span><span class="sxs-lookup"><span data-stu-id="bfd65-126">None</span></span>

## <span data-ttu-id="bfd65-127">출력</span><span class="sxs-lookup"><span data-stu-id="bfd65-127">OUTPUTS</span></span>

### <span data-ttu-id="bfd65-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="bfd65-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="bfd65-129">이 cmdlet은 *Waitforcomplete* 매개 변수를 지정 하는 경우 **Storageaccountcredentialresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="bfd65-130">이 매개 변수를 지정 하지 않으면 cmdlet이 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="bfd65-131">**Storageaccountcredentialresponse** 에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfd65-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="bfd65-132">**Cloudtype** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="bfd65-133">**호스트 이름** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="bfd65-134">**InstanceId** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="bfd65-135">**IsDefault** ( **부울** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="bfd65-136">**위치** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="bfd65-137">**로그인** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="bfd65-138">**Name** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="bfd65-139">**Operationinprogress** ( **operationinprogress** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="bfd65-140">**암호** ( **문자열** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="bfd65-141">**Password. Cert손도장** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="bfd65-142">**UseSSL** ( **부울** )</span><span class="sxs-lookup"><span data-stu-id="bfd65-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="bfd65-143">**(** **Int** ).</span><span class="sxs-lookup"><span data-stu-id="bfd65-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="bfd65-144">상속자</span><span class="sxs-lookup"><span data-stu-id="bfd65-144">NOTES</span></span>

## <span data-ttu-id="bfd65-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfd65-145">RELATED LINKS</span></span>

[<span data-ttu-id="bfd65-146">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bfd65-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="bfd65-147">새-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bfd65-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="bfd65-148">-AzureStorSimpleStorageAccountCredential 제거</span><span class="sxs-lookup"><span data-stu-id="bfd65-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


