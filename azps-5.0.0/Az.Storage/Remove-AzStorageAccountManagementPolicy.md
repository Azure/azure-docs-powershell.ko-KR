---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226045"
---
# <span data-ttu-id="cc074-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cc074-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="cc074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc074-102">SYNOPSIS</span></span>
<span data-ttu-id="cc074-103">Azure 저장소 계정의 관리 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="cc074-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc074-104">SYNTAX</span></span>

### <span data-ttu-id="cc074-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cc074-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc074-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cc074-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc074-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cc074-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc074-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="cc074-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc074-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cc074-109">DESCRIPTION</span></span>
<span data-ttu-id="cc074-110">**AzStorageAccountManagementPolicy** Cmdlet은 Azure 저장소 계정의 관리 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="cc074-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cc074-111">EXAMPLES</span></span>

### <span data-ttu-id="cc074-112">예제 1: 저장소 계정의 관리 정책 제거</span><span class="sxs-lookup"><span data-stu-id="cc074-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="cc074-113">이 명령은 저장소 계정의 관리 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="cc074-114">변수</span><span class="sxs-lookup"><span data-stu-id="cc074-114">PARAMETERS</span></span>

### <span data-ttu-id="cc074-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc074-115">-DefaultProfile</span></span>
<span data-ttu-id="cc074-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc074-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc074-117">-InputObject</span></span>
<span data-ttu-id="cc074-118">제거할 관리 개체</span><span class="sxs-lookup"><span data-stu-id="cc074-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="cc074-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc074-119">-PassThru</span></span>
<span data-ttu-id="cc074-120">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cc074-121">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cc074-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc074-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc074-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="cc074-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc074-124">-StorageAccount</span></span>
<span data-ttu-id="cc074-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="cc074-125">Storage account object</span></span>

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

### <span data-ttu-id="cc074-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cc074-126">-StorageAccountName</span></span>
<span data-ttu-id="cc074-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="cc074-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cc074-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="cc074-129">저장소 계정 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="cc074-130">-확인</span><span class="sxs-lookup"><span data-stu-id="cc074-130">-Confirm</span></span>
<span data-ttu-id="cc074-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc074-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc074-132">-WhatIf</span></span>
<span data-ttu-id="cc074-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc074-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc074-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc074-135">CommonParameters</span></span>
<span data-ttu-id="cc074-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc074-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc074-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc074-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc074-138">입력</span><span class="sxs-lookup"><span data-stu-id="cc074-138">INPUTS</span></span>

### <span data-ttu-id="cc074-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc074-139">System.String</span></span>

## <span data-ttu-id="cc074-140">출력</span><span class="sxs-lookup"><span data-stu-id="cc074-140">OUTPUTS</span></span>

### <span data-ttu-id="cc074-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cc074-141">System.Boolean</span></span>

## <span data-ttu-id="cc074-142">상속자</span><span class="sxs-lookup"><span data-stu-id="cc074-142">NOTES</span></span>

## <span data-ttu-id="cc074-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc074-143">RELATED LINKS</span></span>
