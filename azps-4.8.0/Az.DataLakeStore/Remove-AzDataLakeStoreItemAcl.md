---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212820"
---
# <span data-ttu-id="578a0-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="578a0-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="578a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578a0-102">SYNOPSIS</span></span>
<span data-ttu-id="578a0-103">Data Lake Store에서 파일 또는 폴더의 ACL을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="578a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="578a0-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="578a0-105">DESCRIPTION</span></span>
<span data-ttu-id="578a0-106">**AzDataLakeStoreItemAcl** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="578a0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="578a0-107">EXAMPLES</span></span>

### <span data-ttu-id="578a0-108">예제 1: 폴더에서 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="578a0-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="578a0-109">이 명령은 ContosoADL account의 루트 디렉터리에 대 한 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="578a0-110">변수</span><span class="sxs-lookup"><span data-stu-id="578a0-110">PARAMETERS</span></span>

### <span data-ttu-id="578a0-111">-계정</span><span class="sxs-lookup"><span data-stu-id="578a0-111">-Account</span></span>
<span data-ttu-id="578a0-112">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="578a0-113">-기본</span><span class="sxs-lookup"><span data-stu-id="578a0-113">-Default</span></span>
<span data-ttu-id="578a0-114">Cmdlet이 파일 또는 폴더에 대 한 기본 ACL을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="578a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578a0-115">-DefaultProfile</span></span>
<span data-ttu-id="578a0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="578a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="578a0-117">-Force</span></span>
<span data-ttu-id="578a0-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="578a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="578a0-119">-PassThru</span></span>
<span data-ttu-id="578a0-120">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="578a0-121">-Path</span><span class="sxs-lookup"><span data-stu-id="578a0-121">-Path</span></span>
<span data-ttu-id="578a0-122">루트 디렉터리 (/)부터 시작 하 여 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="578a0-123">-확인</span><span class="sxs-lookup"><span data-stu-id="578a0-123">-Confirm</span></span>
<span data-ttu-id="578a0-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578a0-125">-WhatIf</span></span>
<span data-ttu-id="578a0-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578a0-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578a0-128">CommonParameters</span></span>
<span data-ttu-id="578a0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="578a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578a0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578a0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578a0-131">입력</span><span class="sxs-lookup"><span data-stu-id="578a0-131">INPUTS</span></span>

### <span data-ttu-id="578a0-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="578a0-132">System.String</span></span>

### <span data-ttu-id="578a0-133">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="578a0-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="578a0-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="578a0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="578a0-135">출력</span><span class="sxs-lookup"><span data-stu-id="578a0-135">OUTPUTS</span></span>

### <span data-ttu-id="578a0-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="578a0-136">System.Boolean</span></span>

## <span data-ttu-id="578a0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="578a0-137">NOTES</span></span>
* <span data-ttu-id="578a0-138">별칭: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="578a0-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="578a0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="578a0-139">RELATED LINKS</span></span>

[<span data-ttu-id="578a0-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="578a0-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="578a0-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="578a0-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="578a0-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="578a0-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


