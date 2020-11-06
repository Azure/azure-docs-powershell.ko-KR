---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534928"
---
# <span data-ttu-id="74c47-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="74c47-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="74c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c47-102">SYNOPSIS</span></span>
<span data-ttu-id="74c47-103">키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74c47-104">SYNTAX</span></span>

### <span data-ttu-id="74c47-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="74c47-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c47-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="74c47-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c47-107">설명은</span><span class="sxs-lookup"><span data-stu-id="74c47-107">DESCRIPTION</span></span>
<span data-ttu-id="74c47-108">**AzureRmKeyVault** cmdlet은 지정 된 키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="74c47-109">또한 해당 인스턴스에 포함 된 모든 키와 비밀이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="74c47-110">이 cmdlet에 대해 리소스 그룹을 지정 하는 것이 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="74c47-111">예제의</span><span class="sxs-lookup"><span data-stu-id="74c47-111">EXAMPLES</span></span>

### <span data-ttu-id="74c47-112">예제 1: 키 자격 증명 모음 제거</span><span class="sxs-lookup"><span data-stu-id="74c47-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="74c47-113">이 명령은 현재 구독에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="74c47-114">예제 2: 지정 된 리소스 그룹에서 키 보관소 제거</span><span class="sxs-lookup"><span data-stu-id="74c47-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="74c47-115">이 명령은 이름이 지정 된 리소스 그룹에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="74c47-116">리소스 그룹 이름을 지정 하지 않으면 cmdlet이 지정 된 키 보관소를 검색 하 여 현재 구독에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="74c47-117">변수</span><span class="sxs-lookup"><span data-stu-id="74c47-117">PARAMETERS</span></span>

### <span data-ttu-id="74c47-118">-Force</span><span class="sxs-lookup"><span data-stu-id="74c47-118">-Force</span></span>
<span data-ttu-id="74c47-119">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="74c47-120">기본적으로이 cmdlet은 키 자격 증명을 삭제할 것인지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="74c47-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="74c47-121">-InRemovedState</span></span>
<span data-ttu-id="74c47-122">이전에 삭제 된 자격 증명을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-123">-위치</span><span class="sxs-lookup"><span data-stu-id="74c47-123">-Location</span></span>
<span data-ttu-id="74c47-124">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c47-125">-ResourceGroupName</span></span>
<span data-ttu-id="74c47-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="74c47-127">-VaultName</span></span>
<span data-ttu-id="74c47-128">제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-129">-확인</span><span class="sxs-lookup"><span data-stu-id="74c47-129">-Confirm</span></span>
<span data-ttu-id="74c47-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c47-131">-WhatIf</span></span>
<span data-ttu-id="74c47-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c47-133">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c47-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c47-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c47-135">-DefaultProfile</span></span>
<span data-ttu-id="74c47-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c47-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c47-137">CommonParameters</span></span>
<span data-ttu-id="74c47-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74c47-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c47-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c47-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c47-140">입력</span><span class="sxs-lookup"><span data-stu-id="74c47-140">INPUTS</span></span>

## <span data-ttu-id="74c47-141">출력</span><span class="sxs-lookup"><span data-stu-id="74c47-141">OUTPUTS</span></span>

## <span data-ttu-id="74c47-142">상속자</span><span class="sxs-lookup"><span data-stu-id="74c47-142">NOTES</span></span>

## <span data-ttu-id="74c47-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74c47-143">RELATED LINKS</span></span>

[<span data-ttu-id="74c47-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="74c47-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="74c47-145">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="74c47-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
