---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489056"
---
# <span data-ttu-id="caf0c-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="caf0c-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="caf0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf0c-102">SYNOPSIS</span></span>
<span data-ttu-id="caf0c-103">Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수 권한을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="caf0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="caf0c-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caf0c-105">설명</span><span class="sxs-lookup"><span data-stu-id="caf0c-105">DESCRIPTION</span></span>
<span data-ttu-id="caf0c-106">**Set-AzDataLakeStoreItemPermission** cmdlet은 Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="caf0c-107">예제</span><span class="sxs-lookup"><span data-stu-id="caf0c-107">EXAMPLES</span></span>

### <span data-ttu-id="caf0c-108">예제 1: 항목에 대한 사용 권한 8진수 설정</span><span class="sxs-lookup"><span data-stu-id="caf0c-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="caf0c-109">이 명령은 파일의 사용 권한 8진을 0770으로 설정합니다. 그러면 고정 비트를 지우고, 파일의 소유자에 대한 읽기/쓰기/실행 권한을 설정하고, 파일의 소유 그룹에 대한 읽기/쓰기/실행 권한을 설정하고, 다른 파일에 대한 읽기/쓰기/실행 권한을 지우는 것으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="caf0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caf0c-110">PARAMETERS</span></span>

### <span data-ttu-id="caf0c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="caf0c-111">-Account</span></span>
<span data-ttu-id="caf0c-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="caf0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf0c-113">-DefaultProfile</span></span>
<span data-ttu-id="caf0c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caf0c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="caf0c-115">-Path</span></span>
<span data-ttu-id="caf0c-116">루트 디렉터리(/)로 시작하는 파일 또는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="caf0c-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="caf0c-117">-Permission</span></span>
<span data-ttu-id="caf0c-118">8진수로 표현된 파일 또는 폴더에 대해 설정할 권한(예: '777')</span><span class="sxs-lookup"><span data-stu-id="caf0c-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf0c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caf0c-119">-Confirm</span></span>
<span data-ttu-id="caf0c-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf0c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf0c-121">-WhatIf</span></span>
<span data-ttu-id="caf0c-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="caf0c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf0c-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf0c-124">CommonParameters</span></span>
<span data-ttu-id="caf0c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="caf0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf0c-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="caf0c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf0c-127">입력</span><span class="sxs-lookup"><span data-stu-id="caf0c-127">INPUTS</span></span>

### <span data-ttu-id="caf0c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="caf0c-128">System.String</span></span>

### <span data-ttu-id="caf0c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="caf0c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="caf0c-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="caf0c-130">System.Int32</span></span>

## <span data-ttu-id="caf0c-131">출력</span><span class="sxs-lookup"><span data-stu-id="caf0c-131">OUTPUTS</span></span>

### <span data-ttu-id="caf0c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="caf0c-132">System.Boolean</span></span>

## <span data-ttu-id="caf0c-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="caf0c-133">NOTES</span></span>
* <span data-ttu-id="caf0c-134">별칭: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="caf0c-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="caf0c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caf0c-135">RELATED LINKS</span></span>

[<span data-ttu-id="caf0c-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="caf0c-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


