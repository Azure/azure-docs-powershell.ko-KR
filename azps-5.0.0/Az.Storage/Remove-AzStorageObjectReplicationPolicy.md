---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215804"
---
# <span data-ttu-id="80863-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="80863-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="80863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80863-102">SYNOPSIS</span></span>
<span data-ttu-id="80863-103">저장소 계정에서 지정 된 개체 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="80863-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80863-104">SYNTAX</span></span>

### <span data-ttu-id="80863-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="80863-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80863-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="80863-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80863-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="80863-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80863-108">설명은</span><span class="sxs-lookup"><span data-stu-id="80863-108">DESCRIPTION</span></span>
<span data-ttu-id="80863-109">**AzStorageObjectReplicationPolicy** Cmdlet은 저장소 계정에서 지정 된 개체 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="80863-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80863-110">EXAMPLES</span></span>

### <span data-ttu-id="80863-111">예제 1: 저장소 계정에서 특정 policyId를 사용 하 여 개체 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="80863-112">이 명령은 저장소 계정에서 특정 policyId를 사용 하 여 개체 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="80863-113">변수</span><span class="sxs-lookup"><span data-stu-id="80863-113">PARAMETERS</span></span>

### <span data-ttu-id="80863-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80863-114">-DefaultProfile</span></span>
<span data-ttu-id="80863-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80863-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80863-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80863-116">-InputObject</span></span>
<span data-ttu-id="80863-117">삭제할 개체 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80863-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80863-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80863-118">-PassThru</span></span>
<span data-ttu-id="80863-119">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="80863-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="80863-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="80863-120">-PolicyId</span></span>
<span data-ttu-id="80863-121">개체 복제 정책 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="80863-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80863-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80863-122">-ResourceGroupName</span></span>
<span data-ttu-id="80863-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80863-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="80863-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="80863-124">-StorageAccount</span></span>
<span data-ttu-id="80863-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="80863-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80863-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="80863-126">-StorageAccountName</span></span>
<span data-ttu-id="80863-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80863-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80863-128">-확인</span><span class="sxs-lookup"><span data-stu-id="80863-128">-Confirm</span></span>
<span data-ttu-id="80863-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80863-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80863-130">-WhatIf</span></span>
<span data-ttu-id="80863-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80863-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80863-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80863-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80863-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80863-133">CommonParameters</span></span>
<span data-ttu-id="80863-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80863-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80863-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80863-136">입력</span><span class="sxs-lookup"><span data-stu-id="80863-136">INPUTS</span></span>

### <span data-ttu-id="80863-137">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80863-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="80863-138">PSObjectReplicationPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="80863-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="80863-139">출력</span><span class="sxs-lookup"><span data-stu-id="80863-139">OUTPUTS</span></span>

### <span data-ttu-id="80863-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="80863-140">System.Boolean</span></span>

## <span data-ttu-id="80863-141">상속자</span><span class="sxs-lookup"><span data-stu-id="80863-141">NOTES</span></span>

## <span data-ttu-id="80863-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80863-142">RELATED LINKS</span></span>
