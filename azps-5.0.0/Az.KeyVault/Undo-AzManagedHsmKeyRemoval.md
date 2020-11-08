---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215280"
---
# <span data-ttu-id="2c716-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2c716-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="2c716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c716-102">SYNOPSIS</span></span>
<span data-ttu-id="2c716-103">관리 되는 HSM의 삭제 된 키를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="2c716-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c716-104">SYNTAX</span></span>

### <span data-ttu-id="2c716-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c716-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c716-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2c716-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c716-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c716-107">DESCRIPTION</span></span>
<span data-ttu-id="2c716-108">**AzManagedHsmKeyRemoval** cmdlet은 이전에 삭제 된 키를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="2c716-109">복구 된 키는 활성화 되며 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="2c716-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2c716-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2c716-111">EXAMPLES</span></span>

### <span data-ttu-id="2c716-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c716-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="2c716-113">이 명령을 사용 하면 이전에 삭제 된 ' testkey001 ' 키가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2c716-114">변수</span><span class="sxs-lookup"><span data-stu-id="2c716-114">PARAMETERS</span></span>

### <span data-ttu-id="2c716-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c716-115">-DefaultProfile</span></span>
<span data-ttu-id="2c716-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c716-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2c716-117">-HsmName</span></span>
<span data-ttu-id="2c716-118">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="2c716-118">HSM name.</span></span> <span data-ttu-id="2c716-119">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c716-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c716-120">-InputObject</span></span>
<span data-ttu-id="2c716-121">삭제 된 키 개체</span><span class="sxs-lookup"><span data-stu-id="2c716-121">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c716-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2c716-122">-Name</span></span>
<span data-ttu-id="2c716-123">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-123">Key name.</span></span>
<span data-ttu-id="2c716-124">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c716-125">-확인</span><span class="sxs-lookup"><span data-stu-id="2c716-125">-Confirm</span></span>
<span data-ttu-id="2c716-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c716-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c716-127">-WhatIf</span></span>
<span data-ttu-id="2c716-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c716-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c716-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c716-130">CommonParameters</span></span>
<span data-ttu-id="2c716-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c716-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c716-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c716-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c716-133">입력</span><span class="sxs-lookup"><span data-stu-id="2c716-133">INPUTS</span></span>

### <span data-ttu-id="2c716-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2c716-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="2c716-135">출력</span><span class="sxs-lookup"><span data-stu-id="2c716-135">OUTPUTS</span></span>

### <span data-ttu-id="2c716-136">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2c716-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="2c716-137">상속자</span><span class="sxs-lookup"><span data-stu-id="2c716-137">NOTES</span></span>

## <span data-ttu-id="2c716-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c716-138">RELATED LINKS</span></span>

[<span data-ttu-id="2c716-139">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="2c716-140">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="2c716-141">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="2c716-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="2c716-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="2c716-144">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2c716-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)