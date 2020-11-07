---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880441"
---
# <span data-ttu-id="4aa0e-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4aa0e-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="4aa0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa0e-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa0e-103">키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aa0e-104">SYNTAX</span></span>

### <span data-ttu-id="4aa0e-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="4aa0e-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa0e-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="4aa0e-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aa0e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4aa0e-107">DESCRIPTION</span></span>
<span data-ttu-id="4aa0e-108">**AzureRmKeyVault** cmdlet은 지정 된 키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="4aa0e-109">또한 해당 인스턴스에 포함 된 모든 키와 비밀이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="4aa0e-110">이 cmdlet에 대해 리소스 그룹을 지정 하는 것이 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="4aa0e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4aa0e-111">EXAMPLES</span></span>

### <span data-ttu-id="4aa0e-112">예제 1: 키 자격 증명 모음 제거</span><span class="sxs-lookup"><span data-stu-id="4aa0e-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="4aa0e-113">이 명령은 현재 구독에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="4aa0e-114">예제 2: 지정 된 리소스 그룹에서 키 보관소 제거</span><span class="sxs-lookup"><span data-stu-id="4aa0e-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="4aa0e-115">이 명령은 이름이 지정 된 리소스 그룹에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="4aa0e-116">리소스 그룹 이름을 지정 하지 않으면 cmdlet이 지정 된 키 보관소를 검색 하 여 현재 구독에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="4aa0e-117">변수</span><span class="sxs-lookup"><span data-stu-id="4aa0e-117">PARAMETERS</span></span>

### <span data-ttu-id="4aa0e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aa0e-118">-AsJob</span></span>
<span data-ttu-id="4aa0e-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4aa0e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4aa0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa0e-120">-DefaultProfile</span></span>
<span data-ttu-id="4aa0e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4aa0e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aa0e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4aa0e-122">-Force</span></span>
<span data-ttu-id="4aa0e-123">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="4aa0e-124">기본적으로이 cmdlet은 키 자격 증명을 삭제할 것인지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="4aa0e-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4aa0e-125">-InRemovedState</span></span>
<span data-ttu-id="4aa0e-126">이전에 삭제 된 자격 증명을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-127">-위치</span><span class="sxs-lookup"><span data-stu-id="4aa0e-127">-Location</span></span>
<span data-ttu-id="4aa0e-128">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-128">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa0e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4aa0e-130">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4aa0e-131">-VaultName</span></span>
<span data-ttu-id="4aa0e-132">제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4aa0e-133">-Confirm</span></span>
<span data-ttu-id="4aa0e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa0e-135">-WhatIf</span></span>
<span data-ttu-id="4aa0e-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa0e-137">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa0e-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa0e-139">CommonParameters</span></span>
<span data-ttu-id="4aa0e-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa0e-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa0e-142">입력</span><span class="sxs-lookup"><span data-stu-id="4aa0e-142">INPUTS</span></span>

## <span data-ttu-id="4aa0e-143">출력</span><span class="sxs-lookup"><span data-stu-id="4aa0e-143">OUTPUTS</span></span>

## <span data-ttu-id="4aa0e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4aa0e-144">NOTES</span></span>

## <span data-ttu-id="4aa0e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aa0e-145">RELATED LINKS</span></span>

[<span data-ttu-id="4aa0e-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4aa0e-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="4aa0e-147">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4aa0e-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
