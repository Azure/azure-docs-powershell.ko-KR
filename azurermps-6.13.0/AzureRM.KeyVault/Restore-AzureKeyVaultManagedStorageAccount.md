---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527927"
---
# <span data-ttu-id="506a7-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="506a7-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="506a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="506a7-102">SYNOPSIS</span></span>
<span data-ttu-id="506a7-103">백업 파일의 키 보관소에 관리 저장소 계정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="506a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="506a7-104">SYNTAX</span></span>

### <span data-ttu-id="506a7-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="506a7-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="506a7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="506a7-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="506a7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="506a7-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="506a7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="506a7-108">DESCRIPTION</span></span>
<span data-ttu-id="506a7-109">**Restore-AzureKeyVaultManagedStorageAccount** cmdlet은 백업 파일에서 지정 된 키 보관소에 관리 되는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="506a7-110">이 관리 저장소 계정은 입력 파일에서 백업한 관리 저장소 계정의 복제본 이며 원본과 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="506a7-111">키 자격 증명 모음에 같은 이름의 관리 저장소 계정이 이미 포함 되어 있는 경우에는 원본에 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="506a7-112">관리 저장소 계정을 복원할 키 보관소는 관리 저장소 계정을 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="506a7-113">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="506a7-114"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="506a7-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="506a7-115">예제의</span><span class="sxs-lookup"><span data-stu-id="506a7-115">EXAMPLES</span></span>

### <span data-ttu-id="506a7-116">예제 1: 백업한 관리 저장소 계정 복원</span><span class="sxs-lookup"><span data-stu-id="506a7-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="506a7-117">이 명령은 백업 파일의 모든 버전을 포함 하 여 관리 되는 저장소 계정을 MyKeyVault 이라는 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="506a7-118">변수</span><span class="sxs-lookup"><span data-stu-id="506a7-118">PARAMETERS</span></span>

### <span data-ttu-id="506a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506a7-119">-DefaultProfile</span></span>
<span data-ttu-id="506a7-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506a7-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="506a7-121">-InputFile</span></span>
<span data-ttu-id="506a7-122">입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-122">Input file.</span></span>
<span data-ttu-id="506a7-123">백업 된 blob을 포함 하는 입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="506a7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="506a7-124">-InputObject</span></span>
<span data-ttu-id="506a7-125">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="506a7-125">KeyVault object</span></span>

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

### <span data-ttu-id="506a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="506a7-126">-ResourceId</span></span>
<span data-ttu-id="506a7-127">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="506a7-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="506a7-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="506a7-128">-VaultName</span></span>
<span data-ttu-id="506a7-129">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="506a7-129">Vault name.</span></span>
<span data-ttu-id="506a7-130">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="506a7-131">-확인</span><span class="sxs-lookup"><span data-stu-id="506a7-131">-Confirm</span></span>
<span data-ttu-id="506a7-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506a7-133">-WhatIf</span></span>
<span data-ttu-id="506a7-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506a7-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506a7-136">CommonParameters</span></span>
<span data-ttu-id="506a7-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="506a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506a7-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506a7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506a7-139">입력</span><span class="sxs-lookup"><span data-stu-id="506a7-139">INPUTS</span></span>

### <span data-ttu-id="506a7-140">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="506a7-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="506a7-141">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="506a7-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="506a7-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="506a7-142">System.String</span></span>

## <span data-ttu-id="506a7-143">출력</span><span class="sxs-lookup"><span data-stu-id="506a7-143">OUTPUTS</span></span>

### <span data-ttu-id="506a7-144">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="506a7-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="506a7-145">상속자</span><span class="sxs-lookup"><span data-stu-id="506a7-145">NOTES</span></span>

## <span data-ttu-id="506a7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="506a7-146">RELATED LINKS</span></span>