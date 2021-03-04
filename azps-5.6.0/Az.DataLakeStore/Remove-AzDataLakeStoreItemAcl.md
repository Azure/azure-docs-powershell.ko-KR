---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971131"
---
# <span data-ttu-id="1f177-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1f177-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="1f177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f177-102">SYNOPSIS</span></span>
<span data-ttu-id="1f177-103">Data Lake Store에서 파일 또는 폴더의 ACL을 지우습니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1f177-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f177-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f177-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f177-105">DESCRIPTION</span></span>
<span data-ttu-id="1f177-106">**Remove-AzDataLakeStoreItemAcl** cmdlet은 Data Lake Store의 파일 또는 폴더의 액세스 제어 목록(ACL)을 지우게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1f177-107">예제</span><span class="sxs-lookup"><span data-stu-id="1f177-107">EXAMPLES</span></span>

### <span data-ttu-id="1f177-108">예제 1: 폴더에서 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="1f177-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="1f177-109">이 명령은 ContosoADL 계정에 대한 루트 디렉터리에 대한 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="1f177-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f177-110">PARAMETERS</span></span>

### <span data-ttu-id="1f177-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1f177-111">-Account</span></span>
<span data-ttu-id="1f177-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="1f177-113">-Default</span><span class="sxs-lookup"><span data-stu-id="1f177-113">-Default</span></span>
<span data-ttu-id="1f177-114">cmdlet이 파일 또는 폴더에 대한 기본 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="1f177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f177-115">-DefaultProfile</span></span>
<span data-ttu-id="1f177-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f177-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f177-117">-Force</span></span>
<span data-ttu-id="1f177-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f177-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f177-119">-PassThru</span></span>
<span data-ttu-id="1f177-120">삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="1f177-121">-Path</span><span class="sxs-lookup"><span data-stu-id="1f177-121">-Path</span></span>
<span data-ttu-id="1f177-122">루트 디렉터리(/)로 시작하여 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1f177-123">-확인</span><span class="sxs-lookup"><span data-stu-id="1f177-123">-Confirm</span></span>
<span data-ttu-id="1f177-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f177-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f177-125">-WhatIf</span></span>
<span data-ttu-id="1f177-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f177-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f177-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f177-128">CommonParameters</span></span>
<span data-ttu-id="1f177-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f177-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f177-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f177-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f177-131">입력</span><span class="sxs-lookup"><span data-stu-id="1f177-131">INPUTS</span></span>

### <span data-ttu-id="1f177-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1f177-132">System.String</span></span>

### <span data-ttu-id="1f177-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1f177-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1f177-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f177-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f177-135">출력</span><span class="sxs-lookup"><span data-stu-id="1f177-135">OUTPUTS</span></span>

### <span data-ttu-id="1f177-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f177-136">System.Boolean</span></span>

## <span data-ttu-id="1f177-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f177-137">NOTES</span></span>
* <span data-ttu-id="1f177-138">별칭: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="1f177-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="1f177-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f177-139">RELATED LINKS</span></span>

[<span data-ttu-id="1f177-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1f177-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="1f177-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1f177-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="1f177-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1f177-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


