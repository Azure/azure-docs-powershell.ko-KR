---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198124"
---
# <span data-ttu-id="36a12-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="36a12-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="36a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a12-102">SYNOPSIS</span></span>
<span data-ttu-id="36a12-103">Data Lake Store에서 파일 또는 폴더의 ACL을 지워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="36a12-104">구문</span><span class="sxs-lookup"><span data-stu-id="36a12-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a12-105">설명</span><span class="sxs-lookup"><span data-stu-id="36a12-105">DESCRIPTION</span></span>
<span data-ttu-id="36a12-106">**Remove-AzDataLakeStoreItemAcl** cmdlet은 Data Lake Store에 있는 파일 또는 폴더의 ACL(액세스 제어 목록)을 지우습니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="36a12-107">예제</span><span class="sxs-lookup"><span data-stu-id="36a12-107">EXAMPLES</span></span>

### <span data-ttu-id="36a12-108">예제 1: 폴더에서 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="36a12-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="36a12-109">이 명령은 ContosoADL 계정에 대한 루트 디렉터리에 대한 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="36a12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a12-110">PARAMETERS</span></span>

### <span data-ttu-id="36a12-111">-Account</span><span class="sxs-lookup"><span data-stu-id="36a12-111">-Account</span></span>
<span data-ttu-id="36a12-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a12-113">-Default</span><span class="sxs-lookup"><span data-stu-id="36a12-113">-Default</span></span>
<span data-ttu-id="36a12-114">cmdlet이 파일 또는 폴더에 대한 기본 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a12-115">-DefaultProfile</span></span>
<span data-ttu-id="36a12-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36a12-117">-Force</span><span class="sxs-lookup"><span data-stu-id="36a12-117">-Force</span></span>
<span data-ttu-id="36a12-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a12-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36a12-119">-PassThru</span></span>
<span data-ttu-id="36a12-120">삭제 작업의 결과를 나타내는 부울 응답이 반환되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a12-121">-Path</span><span class="sxs-lookup"><span data-stu-id="36a12-121">-Path</span></span>
<span data-ttu-id="36a12-122">루트 디렉터리(/)로 시작하는 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a12-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36a12-123">-Confirm</span></span>
<span data-ttu-id="36a12-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a12-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a12-125">-WhatIf</span></span>
<span data-ttu-id="36a12-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36a12-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a12-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a12-128">CommonParameters</span></span>
<span data-ttu-id="36a12-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36a12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a12-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36a12-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a12-131">입력</span><span class="sxs-lookup"><span data-stu-id="36a12-131">INPUTS</span></span>

### <span data-ttu-id="36a12-132">System.String</span><span class="sxs-lookup"><span data-stu-id="36a12-132">System.String</span></span>

### <span data-ttu-id="36a12-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="36a12-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="36a12-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36a12-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36a12-135">출력</span><span class="sxs-lookup"><span data-stu-id="36a12-135">OUTPUTS</span></span>

### <span data-ttu-id="36a12-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36a12-136">System.Boolean</span></span>

## <span data-ttu-id="36a12-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36a12-137">NOTES</span></span>
* <span data-ttu-id="36a12-138">별칭: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="36a12-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="36a12-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36a12-139">RELATED LINKS</span></span>

[<span data-ttu-id="36a12-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="36a12-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="36a12-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="36a12-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="36a12-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="36a12-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


