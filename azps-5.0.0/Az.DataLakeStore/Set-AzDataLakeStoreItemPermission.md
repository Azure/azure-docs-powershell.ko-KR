---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305477"
---
# <span data-ttu-id="28d7b-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="28d7b-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="28d7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="28d7b-103">Data Lake Store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="28d7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28d7b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="28d7b-106">**AzDataLakeStoreItemPermission** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="28d7b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="28d7b-108">예제 1: 항목에 대 한 사용 권한 8 진수 설정</span><span class="sxs-lookup"><span data-stu-id="28d7b-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="28d7b-109">이 명령은 파일에 대 한 사용 권한 8 진수를 0770으로 설정 하 고 파일 소유자에 대 한 읽기/쓰기/실행 권한을 설정 하 고, 파일을 소유 하는 그룹에 대 한 읽기/쓰기/실행 권한을 설정 하 고, 다른에 대 한 읽기/쓰기/실행 권한을 해제 하도록 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="28d7b-110">변수</span><span class="sxs-lookup"><span data-stu-id="28d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="28d7b-111">-계정</span><span class="sxs-lookup"><span data-stu-id="28d7b-111">-Account</span></span>
<span data-ttu-id="28d7b-112">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="28d7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d7b-113">-DefaultProfile</span></span>
<span data-ttu-id="28d7b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28d7b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="28d7b-115">-Path</span></span>
<span data-ttu-id="28d7b-116">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="28d7b-117">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="28d7b-117">-Permission</span></span>
<span data-ttu-id="28d7b-118">파일 또는 폴더에 대해 설정할 사용 권한으로 서 8 진수로 표시 됩니다 (예: ' 777 ').</span><span class="sxs-lookup"><span data-stu-id="28d7b-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="28d7b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="28d7b-119">-Confirm</span></span>
<span data-ttu-id="28d7b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d7b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d7b-121">-WhatIf</span></span>
<span data-ttu-id="28d7b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d7b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d7b-124">CommonParameters</span></span>
<span data-ttu-id="28d7b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d7b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d7b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d7b-127">입력</span><span class="sxs-lookup"><span data-stu-id="28d7b-127">INPUTS</span></span>

### <span data-ttu-id="28d7b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28d7b-128">System.String</span></span>

### <span data-ttu-id="28d7b-129">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="28d7b-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="28d7b-130">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="28d7b-130">System.Int32</span></span>

## <span data-ttu-id="28d7b-131">출력</span><span class="sxs-lookup"><span data-stu-id="28d7b-131">OUTPUTS</span></span>

### <span data-ttu-id="28d7b-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="28d7b-132">System.Boolean</span></span>

## <span data-ttu-id="28d7b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="28d7b-133">NOTES</span></span>
* <span data-ttu-id="28d7b-134">별칭: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="28d7b-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="28d7b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d7b-135">RELATED LINKS</span></span>

[<span data-ttu-id="28d7b-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="28d7b-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


