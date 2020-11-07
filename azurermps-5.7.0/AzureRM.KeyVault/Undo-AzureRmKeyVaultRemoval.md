---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711167"
---
# <span data-ttu-id="d6b70-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="d6b70-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="d6b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b70-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b70-103">삭제 된 키 자격 증명 모음을 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6b70-104">SYNTAX</span></span>

### <span data-ttu-id="d6b70-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6b70-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b70-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b70-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d6b70-107">DESCRIPTION</span></span>
<span data-ttu-id="d6b70-108">**AzureRmKeyVaultRemoval** cmdlet은 이전에 삭제 된 키 자격 증명 모음을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="d6b70-109">복구 후 복구 된 자격 증명 모음이 활성 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="d6b70-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6b70-110">EXAMPLES</span></span>

### <span data-ttu-id="d6b70-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6b70-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="d6b70-112">이 명령은 eastus2 지역 및 ' MyResourceGroup ' 리소스 그룹에서 이전에 삭제 된 키 자격 증명 모음 ' MyKeyVault '을 활성 및 사용 가능한 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="d6b70-113">또한 태그를 새 태그로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="d6b70-114">변수</span><span class="sxs-lookup"><span data-stu-id="d6b70-114">PARAMETERS</span></span>

### <span data-ttu-id="d6b70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b70-115">-DefaultProfile</span></span>
<span data-ttu-id="d6b70-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6b70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6b70-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b70-117">-InputObject</span></span>
<span data-ttu-id="d6b70-118">삭제 된 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="d6b70-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-119">-위치</span><span class="sxs-lookup"><span data-stu-id="d6b70-119">-Location</span></span>
<span data-ttu-id="d6b70-120">삭제 된 자격 증명 모음 원본 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b70-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6b70-122">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-123">태그</span><span class="sxs-lookup"><span data-stu-id="d6b70-123">-Tag</span></span>
<span data-ttu-id="d6b70-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d6b70-125">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="d6b70-125">For example:</span></span>

<span data-ttu-id="d6b70-126">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d6b70-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d6b70-127">-VaultName</span></span>
<span data-ttu-id="d6b70-128">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="d6b70-128">Vault name.</span></span>
<span data-ttu-id="d6b70-129">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d6b70-130">-Confirm</span></span>
<span data-ttu-id="d6b70-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b70-132">-WhatIf</span></span>
<span data-ttu-id="d6b70-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6b70-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b70-135">CommonParameters</span></span>
<span data-ttu-id="d6b70-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b70-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b70-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b70-138">입력</span><span class="sxs-lookup"><span data-stu-id="d6b70-138">INPUTS</span></span>

### <span data-ttu-id="d6b70-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6b70-139">System.String</span></span>
<span data-ttu-id="d6b70-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d6b70-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d6b70-141">출력</span><span class="sxs-lookup"><span data-stu-id="d6b70-141">OUTPUTS</span></span>

### <span data-ttu-id="d6b70-142">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d6b70-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d6b70-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d6b70-143">NOTES</span></span>

## <span data-ttu-id="d6b70-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6b70-144">RELATED LINKS</span></span>

[<span data-ttu-id="d6b70-145">제거-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d6b70-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="d6b70-146">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d6b70-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="d6b70-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d6b70-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
