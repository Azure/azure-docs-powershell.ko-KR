---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: 109a02ac04fe9926ef4510d295c978e01026ade2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538051"
---
# <span data-ttu-id="8eed6-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="8eed6-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="8eed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eed6-102">SYNOPSIS</span></span>
<span data-ttu-id="8eed6-103">백업 작업의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eed6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eed6-104">SYNTAX</span></span>

### <span data-ttu-id="8eed6-105">JobsFiltersSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8eed6-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8eed6-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="8eed6-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eed6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8eed6-107">DESCRIPTION</span></span>
<span data-ttu-id="8eed6-108">**AzureRmBackupJobDetails** Cmdlet은 Azure 백업 작업의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="8eed6-109">이 cmdlet을 사용 하 여 실패 한 작업에 대 한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="8eed6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8eed6-110">EXAMPLES</span></span>

### <span data-ttu-id="8eed6-111">예제 1: 실패 한 작업의 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="8eed6-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="8eed6-112">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="8eed6-113">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8eed6-114">두 번째 명령은 $Vault의 자격 증명 모음에서 실패 한 작업을 가져온 다음 $Jobs 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="8eed6-115">세 번째 작업은 $Jobs 변수에서 첫 번째 작업에 대 한 세부 정보를 가져온 다음 해당 세부 정보를 $JobDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="8eed6-116">마지막 명령은 표준 도트 구문을 사용 하 여 $JobDetails의 **Errordetails** 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="8eed6-117">예제 2: 실패 한 작업에 대 한 권장 작업 표시</span><span class="sxs-lookup"><span data-stu-id="8eed6-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="8eed6-118">이 명령은 첫 번째 예제에서 만든 $JobDetails 변수에서 권장 되는 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="8eed6-119">변수</span><span class="sxs-lookup"><span data-stu-id="8eed6-119">PARAMETERS</span></span>

### <span data-ttu-id="8eed6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eed6-120">-DefaultProfile</span></span>
<span data-ttu-id="8eed6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8eed6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eed6-122">-작업</span><span class="sxs-lookup"><span data-stu-id="8eed6-122">-Job</span></span>
<span data-ttu-id="8eed6-123">이 cmdlet에 대 한 세부 정보를 가져오는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="8eed6-124">**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eed6-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="8eed6-125">-JobId</span></span>
<span data-ttu-id="8eed6-126">이 cmdlet이 세부 정보를 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="8eed6-127">ID는 **AzureRmBackupJob** 개체의 **InstanceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="8eed6-128">**AzureRmBackupJob** 개체를 얻으려면 AzureRmBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eed6-129">-저장실</span><span class="sxs-lookup"><span data-stu-id="8eed6-129">-Vault</span></span>
<span data-ttu-id="8eed6-130">이 cmdlet가 작업 세부 정보를 가져오는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="8eed6-131">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eed6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eed6-132">CommonParameters</span></span>
<span data-ttu-id="8eed6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eed6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eed6-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eed6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eed6-135">입력</span><span class="sxs-lookup"><span data-stu-id="8eed6-135">INPUTS</span></span>

### <span data-ttu-id="8eed6-136">않아야</span><span class="sxs-lookup"><span data-stu-id="8eed6-136">None</span></span>

## <span data-ttu-id="8eed6-137">출력</span><span class="sxs-lookup"><span data-stu-id="8eed6-137">OUTPUTS</span></span>

### <span data-ttu-id="8eed6-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="8eed6-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="8eed6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="8eed6-139">NOTES</span></span>
* <span data-ttu-id="8eed6-140">않아야</span><span class="sxs-lookup"><span data-stu-id="8eed6-140">None</span></span>

## <span data-ttu-id="8eed6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eed6-141">RELATED LINKS</span></span>

[<span data-ttu-id="8eed6-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8eed6-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="8eed6-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8eed6-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


