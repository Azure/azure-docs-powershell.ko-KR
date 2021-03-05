---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 7294d5c48bd8cbc94ac127ac1f1543827dc2937b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995605"
---
# <span data-ttu-id="a5768-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a5768-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="a5768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5768-102">SYNOPSIS</span></span>
<span data-ttu-id="a5768-103">Data Lake Store에서 파일 또는 폴더의 사용 권한 octal을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a5768-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5768-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5768-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5768-105">DESCRIPTION</span></span>
<span data-ttu-id="a5768-106">**Set-AzDataLakeStoreItemPermission** cmdlet은 Data Lake Store의 파일 또는 폴더의 사용 권한 octal을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a5768-107">예제</span><span class="sxs-lookup"><span data-stu-id="a5768-107">EXAMPLES</span></span>

### <span data-ttu-id="a5768-108">예제 1: 항목에 대한 사용 권한 octal 설정</span><span class="sxs-lookup"><span data-stu-id="a5768-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="a5768-109">이 명령은 파일의 사용 권한 octal을 0770으로 설정하여 고정 비트를 지우고, 파일의 소유자에 대한 읽기/쓰기/실행 사용 권한을 설정하고, 파일의 소유 그룹에 대한 읽기/쓰기/실행 사용 권한을 설정하고, 읽기/쓰기/실행 권한을 지우는 것으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="a5768-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5768-110">PARAMETERS</span></span>

### <span data-ttu-id="a5768-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a5768-111">-Account</span></span>
<span data-ttu-id="a5768-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="a5768-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5768-113">-DefaultProfile</span></span>
<span data-ttu-id="a5768-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5768-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a5768-115">-Path</span></span>
<span data-ttu-id="a5768-116">루트 디렉터리(/)로 시작하여 파일 또는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a5768-117">-권한</span><span class="sxs-lookup"><span data-stu-id="a5768-117">-Permission</span></span>
<span data-ttu-id="a5768-118">옥탈로 표현된 파일 또는 폴더에 대해 설정할 권한(예: '777')</span><span class="sxs-lookup"><span data-stu-id="a5768-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="a5768-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a5768-119">-Confirm</span></span>
<span data-ttu-id="a5768-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5768-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5768-121">-WhatIf</span></span>
<span data-ttu-id="a5768-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5768-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5768-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5768-124">CommonParameters</span></span>
<span data-ttu-id="a5768-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5768-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5768-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5768-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5768-127">입력</span><span class="sxs-lookup"><span data-stu-id="a5768-127">INPUTS</span></span>

### <span data-ttu-id="a5768-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a5768-128">System.String</span></span>

### <span data-ttu-id="a5768-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a5768-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a5768-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a5768-130">System.Int32</span></span>

## <span data-ttu-id="a5768-131">출력</span><span class="sxs-lookup"><span data-stu-id="a5768-131">OUTPUTS</span></span>

### <span data-ttu-id="a5768-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5768-132">System.Boolean</span></span>

## <span data-ttu-id="a5768-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5768-133">NOTES</span></span>
* <span data-ttu-id="a5768-134">별칭: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a5768-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="a5768-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5768-135">RELATED LINKS</span></span>

[<span data-ttu-id="a5768-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="a5768-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


