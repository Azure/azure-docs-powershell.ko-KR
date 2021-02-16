---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197452"
---
# <span data-ttu-id="a7998-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="a7998-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="a7998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7998-102">SYNOPSIS</span></span>
<span data-ttu-id="a7998-103">시스템과 Azure 파일 동기화 간의 잠재적인 호환성 문제를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="a7998-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7998-104">SYNTAX</span></span>

### <span data-ttu-id="a7998-105">PathBased(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7998-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="a7998-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="a7998-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="a7998-107">설명</span><span class="sxs-lookup"><span data-stu-id="a7998-107">DESCRIPTION</span></span>
<span data-ttu-id="a7998-108">**Invoke-AzStorageSyncCompatibilityCheck** cmdlet은 시스템과 Azure 파일 동기화 간의 잠재적인 호환성 문제를 확인합니다. 로컬 또는 원격 경로가 주어지면 시스템 및 파일 네임스페이스에서 유효성 검사 집합을 수행한 다음 발견된 호환성 문제를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="a7998-109">시스템 검사:</span><span class="sxs-lookup"><span data-stu-id="a7998-109">System checks:</span></span>
- <span data-ttu-id="a7998-110">OS 호환성 파일 네임스페이스 확인:</span><span class="sxs-lookup"><span data-stu-id="a7998-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="a7998-111">비지원 문자</span><span class="sxs-lookup"><span data-stu-id="a7998-111">Unsupported characters</span></span>
- <span data-ttu-id="a7998-112">최대 파일 크기</span><span class="sxs-lookup"><span data-stu-id="a7998-112">Maximum file size</span></span>
- <span data-ttu-id="a7998-113">최대 경로 길이</span><span class="sxs-lookup"><span data-stu-id="a7998-113">Maximum path length</span></span>
- <span data-ttu-id="a7998-114">최대 파일 길이</span><span class="sxs-lookup"><span data-stu-id="a7998-114">Maximum file length</span></span>
- <span data-ttu-id="a7998-115">최대 데이터 세트 크기</span><span class="sxs-lookup"><span data-stu-id="a7998-115">Maximum dataset size</span></span>
- <span data-ttu-id="a7998-116">최대 디렉터리 깊이</span><span class="sxs-lookup"><span data-stu-id="a7998-116">Maximum directory depth</span></span>

## <span data-ttu-id="a7998-117">예제</span><span class="sxs-lookup"><span data-stu-id="a7998-117">EXAMPLES</span></span>

### <span data-ttu-id="a7998-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7998-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="a7998-119">이 명령은 시스템과 C:\DATA의 파일 및 폴더의 호환성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="a7998-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="a7998-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="a7998-121">이 명령은 C:\DATA에서 파일 및 폴더의 호환성을 검사하지만 시스템 호환성 검사를 수행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="a7998-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="a7998-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="a7998-123">이 명령은 시스템과 C:\DATA의 파일 및 폴더의 호환성을 확인한 다음 결과를 C:\results로 CSV 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="a7998-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7998-124">PARAMETERS</span></span>

### <span data-ttu-id="a7998-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="a7998-125">-ComputerName</span></span>
<span data-ttu-id="a7998-126">이 확인을 수행하는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7998-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="a7998-127">-Credential</span></span>
<span data-ttu-id="a7998-128">유효성을 검사하는 공유에 대한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7998-129">-Path</span><span class="sxs-lookup"><span data-stu-id="a7998-129">-Path</span></span>
<span data-ttu-id="a7998-130">유효성을 검사하는 공유의 UNC 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7998-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="a7998-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="a7998-132">파일 네임스페이스 유효성 검사를 건너뛰고 시스템 유효성 검사만 수행하기 위해 이 플래그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7998-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="a7998-133">-SkipSystemChecks</span></span>
<span data-ttu-id="a7998-134">시스템 유효성 검사를 건너뛰고 파일 네임스페이스 유효성 검사만 수행하기 위해 이 플래그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7998-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7998-135">CommonParameters</span></span>
<span data-ttu-id="a7998-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7998-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7998-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a7998-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7998-138">입력</span><span class="sxs-lookup"><span data-stu-id="a7998-138">INPUTS</span></span>

### <span data-ttu-id="a7998-139">없음</span><span class="sxs-lookup"><span data-stu-id="a7998-139">None</span></span>

## <span data-ttu-id="a7998-140">출력</span><span class="sxs-lookup"><span data-stu-id="a7998-140">OUTPUTS</span></span>

### <span data-ttu-id="a7998-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="a7998-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="a7998-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7998-142">NOTES</span></span>
* <span data-ttu-id="a7998-143">키워드: azure, Az, arm, 리소스, 관리, 저장소ync, 파일ync</span><span class="sxs-lookup"><span data-stu-id="a7998-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="a7998-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7998-144">RELATED LINKS</span></span>
