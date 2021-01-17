---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491328"
---
# <span data-ttu-id="18749-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="18749-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="18749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18749-102">SYNOPSIS</span></span>
<span data-ttu-id="18749-103">Azure Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="18749-104">구문</span><span class="sxs-lookup"><span data-stu-id="18749-104">SYNTAX</span></span>

### <span data-ttu-id="18749-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="18749-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18749-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="18749-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18749-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="18749-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18749-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="18749-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18749-109">설명</span><span class="sxs-lookup"><span data-stu-id="18749-109">DESCRIPTION</span></span>
<span data-ttu-id="18749-110">**Remove-AzStorageAccountManagementPolicy** cmdlet은 Azure Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="18749-111">예제</span><span class="sxs-lookup"><span data-stu-id="18749-111">EXAMPLES</span></span>

### <span data-ttu-id="18749-112">예제 1: Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="18749-113">이 명령은 Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="18749-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18749-114">PARAMETERS</span></span>

### <span data-ttu-id="18749-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18749-115">-DefaultProfile</span></span>
<span data-ttu-id="18749-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18749-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18749-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18749-117">-InputObject</span></span>
<span data-ttu-id="18749-118">제거할 관리 개체</span><span class="sxs-lookup"><span data-stu-id="18749-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18749-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18749-119">-PassThru</span></span>
<span data-ttu-id="18749-120">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="18749-121">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18749-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="18749-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18749-122">-ResourceGroupName</span></span>
<span data-ttu-id="18749-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18749-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="18749-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="18749-124">-StorageAccount</span></span>
<span data-ttu-id="18749-125">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="18749-125">Storage account object</span></span>

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

### <span data-ttu-id="18749-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="18749-126">-StorageAccountName</span></span>
<span data-ttu-id="18749-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18749-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="18749-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="18749-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="18749-129">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="18749-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18749-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18749-130">-Confirm</span></span>
<span data-ttu-id="18749-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18749-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18749-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18749-132">-WhatIf</span></span>
<span data-ttu-id="18749-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="18749-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18749-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18749-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18749-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18749-135">CommonParameters</span></span>
<span data-ttu-id="18749-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18749-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18749-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18749-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18749-138">입력</span><span class="sxs-lookup"><span data-stu-id="18749-138">INPUTS</span></span>

### <span data-ttu-id="18749-139">System.String</span><span class="sxs-lookup"><span data-stu-id="18749-139">System.String</span></span>

## <span data-ttu-id="18749-140">출력</span><span class="sxs-lookup"><span data-stu-id="18749-140">OUTPUTS</span></span>

### <span data-ttu-id="18749-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18749-141">System.Boolean</span></span>

## <span data-ttu-id="18749-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18749-142">NOTES</span></span>

## <span data-ttu-id="18749-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18749-143">RELATED LINKS</span></span>
