---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495437"
---
# <span data-ttu-id="712ab-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="712ab-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="712ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712ab-102">SYNOPSIS</span></span>
<span data-ttu-id="712ab-103">백업 파일에서 키 자격 증명 모음의 관리되는 저장소 계정을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="712ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="712ab-104">SYNTAX</span></span>

### <span data-ttu-id="712ab-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="712ab-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="712ab-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="712ab-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="712ab-108">설명</span><span class="sxs-lookup"><span data-stu-id="712ab-108">DESCRIPTION</span></span>
<span data-ttu-id="712ab-109">**Restore-AzKeyVaultManagedStorageAccount** cmdlet은 백업 파일에서 지정된 키 자격 증명 모음에 관리되는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="712ab-110">이 관리되는 저장소 계정은 입력 파일에서 백업된 관리 저장소 계정의 복제본으로, 원래 계정과 동일한 이름을 습니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="712ab-111">Key Vault에 동일한 이름의 관리되는 저장소 계정이 이미 포함되어 있는 경우 이 cmdlet은 원본을 덮어써는 대신 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="712ab-112">관리되는 저장소 계정을 복원하는 키 자격 증명 모음은 관리되는 저장소 계정을 백업한 키 자격 증명 모음과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="712ab-113">그러나 Key Vault는 동일한 구독을 사용하며 동일한 지역(예: 북아메리카)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="712ab-114">Azure 지역을 지역에 매핑하는 경우 Microsoft Azure 보안 센터를 https://azure.microsoft.com/support/trust-center/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="712ab-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="712ab-115">예제</span><span class="sxs-lookup"><span data-stu-id="712ab-115">EXAMPLES</span></span>

### <span data-ttu-id="712ab-116">예제 1: 백업된 관리되는 저장소 계정 복원</span><span class="sxs-lookup"><span data-stu-id="712ab-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="712ab-117">이 명령은 Backup.blob이라는 백업 파일에서 MyKeyVault라는 키 자격 증명 모음으로 모든 버전을 포함한 관리되는 저장소 계정을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="712ab-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="712ab-118">PARAMETERS</span></span>

### <span data-ttu-id="712ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712ab-119">-DefaultProfile</span></span>
<span data-ttu-id="712ab-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="712ab-121">-InputFile</span></span>
<span data-ttu-id="712ab-122">입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-122">Input file.</span></span>
<span data-ttu-id="712ab-123">백업된 Blob을 포함하는 입력 파일</span><span class="sxs-lookup"><span data-stu-id="712ab-123">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="712ab-124">-InputObject</span></span>
<span data-ttu-id="712ab-125">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="712ab-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="712ab-126">-ResourceId</span></span>
<span data-ttu-id="712ab-127">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="712ab-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="712ab-128">-VaultName</span></span>
<span data-ttu-id="712ab-129">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-129">Vault name.</span></span>
<span data-ttu-id="712ab-130">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="712ab-131">-Confirm</span></span>
<span data-ttu-id="712ab-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712ab-133">-WhatIf</span></span>
<span data-ttu-id="712ab-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="712ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712ab-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712ab-136">CommonParameters</span></span>
<span data-ttu-id="712ab-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="712ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712ab-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="712ab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712ab-139">입력</span><span class="sxs-lookup"><span data-stu-id="712ab-139">INPUTS</span></span>

### <span data-ttu-id="712ab-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="712ab-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="712ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="712ab-141">System.String</span></span>

## <span data-ttu-id="712ab-142">출력</span><span class="sxs-lookup"><span data-stu-id="712ab-142">OUTPUTS</span></span>

### <span data-ttu-id="712ab-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="712ab-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="712ab-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="712ab-144">NOTES</span></span>

## <span data-ttu-id="712ab-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="712ab-145">RELATED LINKS</span></span>
