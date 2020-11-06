---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 5d030f68bfc154dee6d5cd3e98c5eced33e42270
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532299"
---
# <span data-ttu-id="dd837-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="dd837-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="dd837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd837-102">SYNOPSIS</span></span>
<span data-ttu-id="dd837-103">Data Lake Store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd837-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd837-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd837-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd837-105">DESCRIPTION</span></span>
<span data-ttu-id="dd837-106">**AzureRmDataLakeStoreItemPermission** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dd837-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dd837-107">EXAMPLES</span></span>

### <span data-ttu-id="dd837-108">예제 1: 항목에 대 한 사용 권한 8 진수 설정</span><span class="sxs-lookup"><span data-stu-id="dd837-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="dd837-109">이 명령은 파일에 대 한 사용 권한 8 진수를 0770으로 설정 하 고 파일 소유자에 대 한 읽기/쓰기/실행 권한을 설정 하 고, 파일을 소유 하는 그룹에 대 한 읽기/쓰기/실행 권한을 설정 하 고, 다른에 대 한 읽기/쓰기/실행 권한을 해제 하도록 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="dd837-110">변수</span><span class="sxs-lookup"><span data-stu-id="dd837-110">PARAMETERS</span></span>

### <span data-ttu-id="dd837-111">-계정</span><span class="sxs-lookup"><span data-stu-id="dd837-111">-Account</span></span>
<span data-ttu-id="dd837-112">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="dd837-113">-Path</span><span class="sxs-lookup"><span data-stu-id="dd837-113">-Path</span></span>
<span data-ttu-id="dd837-114">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="dd837-115">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="dd837-115">-Permission</span></span>
<span data-ttu-id="dd837-116">파일 또는 폴더에 대해 설정할 사용 권한으로 서 8 진수로 표시 됩니다 (예: ' 777 ').</span><span class="sxs-lookup"><span data-stu-id="dd837-116">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="dd837-117">-확인</span><span class="sxs-lookup"><span data-stu-id="dd837-117">-Confirm</span></span>
<span data-ttu-id="dd837-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd837-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd837-119">-WhatIf</span></span>
<span data-ttu-id="dd837-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd837-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd837-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd837-122">-DefaultProfile</span></span>
<span data-ttu-id="dd837-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd837-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd837-124">CommonParameters</span></span>
<span data-ttu-id="dd837-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd837-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd837-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd837-127">입력</span><span class="sxs-lookup"><span data-stu-id="dd837-127">INPUTS</span></span>

## <span data-ttu-id="dd837-128">출력</span><span class="sxs-lookup"><span data-stu-id="dd837-128">OUTPUTS</span></span>

### <span data-ttu-id="dd837-129">부울</span><span class="sxs-lookup"><span data-stu-id="dd837-129">bool</span></span>
<span data-ttu-id="dd837-130">권한이 성공적으로 업데이트 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd837-130">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="dd837-131">상속자</span><span class="sxs-lookup"><span data-stu-id="dd837-131">NOTES</span></span>
* <span data-ttu-id="dd837-132">별칭: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="dd837-132">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="dd837-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd837-133">RELATED LINKS</span></span>

[<span data-ttu-id="dd837-134">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="dd837-134">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


