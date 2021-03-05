---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: 102f1ebc6152bb521bd1f9c7214a6c48ee61a274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015835"
---
# <span data-ttu-id="85a9e-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="85a9e-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="85a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="85a9e-103">Storage 계정의 모든 사용자 위임 키를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="85a9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="85a9e-104">SYNTAX</span></span>

### <span data-ttu-id="85a9e-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="85a9e-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a9e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="85a9e-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a9e-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="85a9e-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a9e-108">설명</span><span class="sxs-lookup"><span data-stu-id="85a9e-108">DESCRIPTION</span></span>
<span data-ttu-id="85a9e-109">**Revoke-AzStorageAccountUserDelegationKeys** cmdlet은 Storage 계정의 모든 사용자 위임 키를 해지하기 때문에 Storage 계정의 모든 ID SAS 토큰도 해지됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="85a9e-110">예제</span><span class="sxs-lookup"><span data-stu-id="85a9e-110">EXAMPLES</span></span>

### <span data-ttu-id="85a9e-111">예제 1: Storage 계정의 모든 사용자 위임 키 해지</span><span class="sxs-lookup"><span data-stu-id="85a9e-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="85a9e-112">이 예제에서는 Storage 계정의 모든 사용자 위임 키를 해지하기 때문에 사용자 위임 키에서 생성된 모든 ID SAS 토큰도 해지됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="85a9e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85a9e-113">PARAMETERS</span></span>

### <span data-ttu-id="85a9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a9e-114">-DefaultProfile</span></span>
<span data-ttu-id="85a9e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a9e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85a9e-116">-InputObject</span></span>
<span data-ttu-id="85a9e-117">New-AzStorageAccount의 Get_AzStorageAccount 저장소 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a9e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85a9e-118">-PassThru</span></span>
<span data-ttu-id="85a9e-119">일반적으로 이 cmdlet은 성공적으로 완료할 때 출력을 반환하지 않습니다. 이 매개 변수는 cmdlet이 성공적으로 완료할 때 값($true)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="85a9e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a9e-120">-ResourceGroupName</span></span>
<span data-ttu-id="85a9e-121">저장소 계정 리소스를 포함하는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a9e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85a9e-122">-ResourceId</span></span>
<span data-ttu-id="85a9e-123">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a9e-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85a9e-124">-StorageAccountName</span></span>
<span data-ttu-id="85a9e-125">저장소 계정 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a9e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="85a9e-126">-Confirm</span></span>
<span data-ttu-id="85a9e-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a9e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a9e-128">-WhatIf</span></span>
<span data-ttu-id="85a9e-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a9e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a9e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a9e-131">CommonParameters</span></span>
<span data-ttu-id="85a9e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85a9e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a9e-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="85a9e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a9e-134">입력</span><span class="sxs-lookup"><span data-stu-id="85a9e-134">INPUTS</span></span>

### <span data-ttu-id="85a9e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85a9e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="85a9e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="85a9e-136">System.String</span></span>

## <span data-ttu-id="85a9e-137">출력</span><span class="sxs-lookup"><span data-stu-id="85a9e-137">OUTPUTS</span></span>

### <span data-ttu-id="85a9e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85a9e-138">System.Boolean</span></span>

## <span data-ttu-id="85a9e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85a9e-139">NOTES</span></span>

## <span data-ttu-id="85a9e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85a9e-140">RELATED LINKS</span></span>
