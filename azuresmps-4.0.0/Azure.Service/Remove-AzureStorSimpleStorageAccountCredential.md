---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046449"
---
# <span data-ttu-id="accc7-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="accc7-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="accc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="accc7-102">SYNOPSIS</span></span>
<span data-ttu-id="accc7-103">기존 저장소 계정 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="accc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="accc7-104">SYNTAX</span></span>

### <span data-ttu-id="accc7-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="accc7-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="accc7-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="accc7-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="accc7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="accc7-107">DESCRIPTION</span></span>
<span data-ttu-id="accc7-108">**제거-AzureStorSimpleStorageAccountCredential** cmdlet은 기존 저장소 계정 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="accc7-109">이름을 기준으로 계정을 지정 하거나 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 하 여 삭제할 **storageaccountcredential** 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="accc7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="accc7-110">EXAMPLES</span></span>

### <span data-ttu-id="accc7-111">예제 1: 저장소 계정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="accc7-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="accc7-112">이 명령은 ContosoStorage07 이라는 저장소 계정에 대 한 계정 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="accc7-113">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="accc7-114">Cmdlet은 확인 메시지를 표시 하지 않고 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="accc7-115">예제 2: 파이프라인 연산자를 사용 하 여 저장소 계정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="accc7-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="accc7-116">이 명령은 **Get-Azurestorsimplestoragecredential** cmdlet을 사용 하 여 ContosoStorage07 이라는 저장소 계정을 가져온 다음 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="accc7-117">현재 cmdlet은 해당 저장소 계정에 대 한 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="accc7-118">이 명령은 *Waitforcomplete* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="accc7-119">Cmdlet은 제거 작업을 완료할 때까지 콘솔에 컨트롤을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="accc7-120">변수</span><span class="sxs-lookup"><span data-stu-id="accc7-120">PARAMETERS</span></span>

### <span data-ttu-id="accc7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="accc7-121">-Force</span></span>
<span data-ttu-id="accc7-122">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="accc7-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="accc7-123">-Profile</span></span>
<span data-ttu-id="accc7-124">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="accc7-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="accc7-125">-SAC</span></span>
<span data-ttu-id="accc7-126">제거할 **Storageaccountcredential** 개체로 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="accc7-127">**Storageaccountcredential** 개체를 가져오려면 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="accc7-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="accc7-128">-StorageAccountName</span></span>
<span data-ttu-id="accc7-129">삭제할 저장소 계정 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accc7-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="accc7-130">-WaitForComplete</span></span>
<span data-ttu-id="accc7-131">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="accc7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accc7-132">CommonParameters</span></span>
<span data-ttu-id="accc7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accc7-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="accc7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accc7-135">입력</span><span class="sxs-lookup"><span data-stu-id="accc7-135">INPUTS</span></span>

### <span data-ttu-id="accc7-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="accc7-136">StorageAccountCredential</span></span>
<span data-ttu-id="accc7-137">이 cmdlet은 파이프라인을 사용 하 여 **Storageaccountcredential** 개체를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="accc7-138">출력</span><span class="sxs-lookup"><span data-stu-id="accc7-138">OUTPUTS</span></span>

### <span data-ttu-id="accc7-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="accc7-139">TaskStatusInfo</span></span>
<span data-ttu-id="accc7-140">*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="accc7-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="accc7-141">상속자</span><span class="sxs-lookup"><span data-stu-id="accc7-141">NOTES</span></span>

## <span data-ttu-id="accc7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="accc7-142">RELATED LINKS</span></span>

[<span data-ttu-id="accc7-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="accc7-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="accc7-144">새-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="accc7-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="accc7-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="accc7-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="accc7-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="accc7-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


