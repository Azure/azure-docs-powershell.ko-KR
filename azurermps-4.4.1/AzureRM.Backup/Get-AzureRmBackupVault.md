---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528287"
---
# <span data-ttu-id="b4011-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b4011-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="b4011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4011-102">SYNOPSIS</span></span>
<span data-ttu-id="b4011-103">백업 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4011-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4011-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4011-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4011-105">DESCRIPTION</span></span>
<span data-ttu-id="b4011-106">**Get-AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="b4011-107">이 cmdlet은 다른 cmdlet에 사용할 **AzureRmBackupVault** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="b4011-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b4011-108">EXAMPLES</span></span>

### <span data-ttu-id="b4011-109">예제 1: 모든 백업 자격 증명 모음 보기</span><span class="sxs-lookup"><span data-stu-id="b4011-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="b4011-110">이 명령은 모든 Azure Backup 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="b4011-111">예제 2: 미국에서 만든 모든 볼트 보기</span><span class="sxs-lookup"><span data-stu-id="b4011-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="b4011-112">이 명령은 모든 백업 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="b4011-113">파이프라인 연산자를 사용 하 여이 명령을 Where-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4011-114">해당 cmdlet은 **Region** 속성을 기준으로 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="b4011-115">자세한 내용은을 입력 `Get-Help Where-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4011-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="b4011-116">예제 3: 특정 자격 증명 모음 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4011-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="b4011-117">이 명령은 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="b4011-118">예제 4: 로컬에서 중복 저장소를 사용 하는 자격 증명 모음 수 계산</span><span class="sxs-lookup"><span data-stu-id="b4011-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="b4011-119">이 명령은 모든 Azure Backup 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="b4011-120">명령이 해당 위치에 **저장** 속성을 기준으로 결과를 필터링 하는 **개체를 여기** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="b4011-121">Measure-Object LocallyRedundant 값이 있는 명령을 해당 명령에 전달 하 여 결과를 계산 하는 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="b4011-122">자세한 내용은을 입력 `Get-Help Measure-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4011-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="b4011-123">변수</span><span class="sxs-lookup"><span data-stu-id="b4011-123">PARAMETERS</span></span>

### <span data-ttu-id="b4011-124">-이름</span><span class="sxs-lookup"><span data-stu-id="b4011-124">-Name</span></span>
<span data-ttu-id="b4011-125">이 cmdlet이 가져오는 백업 자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="b4011-126">두 개 이상의 백업 자격 증명 모음이 동일한 이름을 가진 경우이 cmdlet은 모두 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="b4011-127">*ResourceGroupName* 매개 변수를 지정 하 여 고유한 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4011-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4011-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4011-129">이 cmdlet이 백업 자격 증명 모음을 가져오는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4011-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4011-130">-DefaultProfile</span></span>
<span data-ttu-id="b4011-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4011-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4011-132">CommonParameters</span></span>
<span data-ttu-id="b4011-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4011-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4011-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4011-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4011-135">입력</span><span class="sxs-lookup"><span data-stu-id="b4011-135">INPUTS</span></span>

## <span data-ttu-id="b4011-136">출력</span><span class="sxs-lookup"><span data-stu-id="b4011-136">OUTPUTS</span></span>

### <span data-ttu-id="b4011-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b4011-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="b4011-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b4011-138">NOTES</span></span>
* <span data-ttu-id="b4011-139">않아야</span><span class="sxs-lookup"><span data-stu-id="b4011-139">None</span></span>

## <span data-ttu-id="b4011-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4011-140">RELATED LINKS</span></span>

[<span data-ttu-id="b4011-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b4011-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b4011-142">새로운 AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b4011-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="b4011-143">제거-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b4011-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="b4011-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b4011-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


