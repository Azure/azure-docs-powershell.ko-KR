---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877402"
---
# <span data-ttu-id="47551-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="47551-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="47551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47551-102">SYNOPSIS</span></span>
<span data-ttu-id="47551-103">저장소 계정의 모든 사용자 위임 키를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="47551-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="47551-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47551-104">SYNTAX</span></span>

### <span data-ttu-id="47551-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="47551-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47551-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="47551-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47551-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="47551-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47551-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47551-108">DESCRIPTION</span></span>
<span data-ttu-id="47551-109">**AzStorageAccountUserDelegationKeys** Cmdlet은 저장소 계정의 모든 사용자 위임 키를 해지 하므로 저장소 계정의 모든 id sa 토큰만 해지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47551-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="47551-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47551-110">EXAMPLES</span></span>

### <span data-ttu-id="47551-111">예제 1: 저장소 계정의 모든 사용자 위임 키 해지</span><span class="sxs-lookup"><span data-stu-id="47551-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="47551-112">이 예제에서는 저장소 계정의 모든 사용자 위임 키를 해지 하므로 사용자 위임 키에서 생성 된 모든 Id SA 토큰만 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47551-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="47551-113">변수</span><span class="sxs-lookup"><span data-stu-id="47551-113">PARAMETERS</span></span>

### <span data-ttu-id="47551-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47551-114">-DefaultProfile</span></span>
<span data-ttu-id="47551-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47551-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47551-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47551-116">-InputObject</span></span>
<span data-ttu-id="47551-117">Get_AzStorageAccount, AzStorageAccount에 의해 반환 된 저장소 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="47551-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="47551-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47551-118">-PassThru</span></span>
<span data-ttu-id="47551-119">일반적으로이 cmdlet은 성공적으로 완료 될 때 출력을 반환 하지 않습니다 .이 매개 변수는 성공적으로 완료 되 면 cmdlet에서 값 ($true)을 반환 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="47551-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="47551-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47551-120">-ResourceGroupName</span></span>
<span data-ttu-id="47551-121">저장소 계정 리소스가 포함 된 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47551-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="47551-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47551-122">-ResourceId</span></span>
<span data-ttu-id="47551-123">저장소 계정 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="47551-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="47551-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47551-124">-StorageAccountName</span></span>
<span data-ttu-id="47551-125">저장소 계정 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47551-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="47551-126">-확인</span><span class="sxs-lookup"><span data-stu-id="47551-126">-Confirm</span></span>
<span data-ttu-id="47551-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="47551-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47551-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47551-128">-WhatIf</span></span>
<span data-ttu-id="47551-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="47551-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47551-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47551-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47551-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47551-131">CommonParameters</span></span>
<span data-ttu-id="47551-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47551-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47551-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47551-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47551-134">입력</span><span class="sxs-lookup"><span data-stu-id="47551-134">INPUTS</span></span>

### <span data-ttu-id="47551-135">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47551-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="47551-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47551-136">System.String</span></span>

## <span data-ttu-id="47551-137">출력</span><span class="sxs-lookup"><span data-stu-id="47551-137">OUTPUTS</span></span>

### <span data-ttu-id="47551-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="47551-138">System.Boolean</span></span>

## <span data-ttu-id="47551-139">상속자</span><span class="sxs-lookup"><span data-stu-id="47551-139">NOTES</span></span>

## <span data-ttu-id="47551-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47551-140">RELATED LINKS</span></span>
