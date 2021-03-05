---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 671a83ee392f59dc27cff6cc34eeb7df054b3fbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002288"
---
# <span data-ttu-id="09c37-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="09c37-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="09c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c37-102">SYNOPSIS</span></span>
<span data-ttu-id="09c37-103">Azure Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="09c37-104">구문</span><span class="sxs-lookup"><span data-stu-id="09c37-104">SYNTAX</span></span>

### <span data-ttu-id="09c37-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="09c37-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c37-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="09c37-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c37-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09c37-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c37-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="09c37-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c37-109">설명</span><span class="sxs-lookup"><span data-stu-id="09c37-109">DESCRIPTION</span></span>
<span data-ttu-id="09c37-110">**Remove-AzStorageAccountManagementPolicy** cmdlet은 Azure Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="09c37-111">예제</span><span class="sxs-lookup"><span data-stu-id="09c37-111">EXAMPLES</span></span>

### <span data-ttu-id="09c37-112">예제 1: Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="09c37-113">이 명령은 Storage 계정의 관리 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="09c37-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="09c37-114">PARAMETERS</span></span>

### <span data-ttu-id="09c37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c37-115">-DefaultProfile</span></span>
<span data-ttu-id="09c37-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c37-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09c37-117">-InputObject</span></span>
<span data-ttu-id="09c37-118">제거할 관리 개체</span><span class="sxs-lookup"><span data-stu-id="09c37-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="09c37-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09c37-119">-PassThru</span></span>
<span data-ttu-id="09c37-120">이 cmdlet은 작업의 성공을 반영하는 **부울을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="09c37-121">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="09c37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c37-122">-ResourceGroupName</span></span>
<span data-ttu-id="09c37-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="09c37-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="09c37-124">-StorageAccount</span></span>
<span data-ttu-id="09c37-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="09c37-125">Storage account object</span></span>

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

### <span data-ttu-id="09c37-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="09c37-126">-StorageAccountName</span></span>
<span data-ttu-id="09c37-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="09c37-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09c37-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="09c37-129">Storage 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="09c37-130">-확인</span><span class="sxs-lookup"><span data-stu-id="09c37-130">-Confirm</span></span>
<span data-ttu-id="09c37-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c37-132">-WhatIf</span></span>
<span data-ttu-id="09c37-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c37-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c37-135">CommonParameters</span></span>
<span data-ttu-id="09c37-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09c37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c37-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="09c37-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c37-138">입력</span><span class="sxs-lookup"><span data-stu-id="09c37-138">INPUTS</span></span>

### <span data-ttu-id="09c37-139">System.String</span><span class="sxs-lookup"><span data-stu-id="09c37-139">System.String</span></span>

## <span data-ttu-id="09c37-140">출력</span><span class="sxs-lookup"><span data-stu-id="09c37-140">OUTPUTS</span></span>

### <span data-ttu-id="09c37-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09c37-141">System.Boolean</span></span>

## <span data-ttu-id="09c37-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09c37-142">NOTES</span></span>

## <span data-ttu-id="09c37-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09c37-143">RELATED LINKS</span></span>
