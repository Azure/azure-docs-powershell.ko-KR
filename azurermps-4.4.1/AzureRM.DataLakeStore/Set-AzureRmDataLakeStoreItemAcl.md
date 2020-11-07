---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711281"
---
# <span data-ttu-id="85276-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="85276-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="85276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85276-102">SYNOPSIS</span></span>
<span data-ttu-id="85276-103">Data Lake Store에서 파일 또는 폴더의 ACL을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85276-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85276-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85276-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85276-105">DESCRIPTION</span></span>
<span data-ttu-id="85276-106">**AzureRmDataLakeStoreItemAcl** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="85276-107">예제의</span><span class="sxs-lookup"><span data-stu-id="85276-107">EXAMPLES</span></span>

### <span data-ttu-id="85276-108">예제 1: 파일 및 폴더에 대 한 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="85276-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="85276-109">첫 번째 명령은 ContosoADL account의 루트 디렉터리에 대 한 ACL을 가져온 다음이를 $ACL 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="85276-110">두 번째 명령은 Test.txt 파일의 ACL을 $ACL의 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="85276-111">변수</span><span class="sxs-lookup"><span data-stu-id="85276-111">PARAMETERS</span></span>

### <span data-ttu-id="85276-112">-계정</span><span class="sxs-lookup"><span data-stu-id="85276-112">-Account</span></span>
<span data-ttu-id="85276-113">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="85276-114">-Acl</span><span class="sxs-lookup"><span data-stu-id="85276-114">-Acl</span></span>
<span data-ttu-id="85276-115">파일 또는 폴더에 대 한 ACL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85276-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85276-116">-PassThru</span></span>
<span data-ttu-id="85276-117">결과 ACL을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85276-117">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="85276-118">-Path</span><span class="sxs-lookup"><span data-stu-id="85276-118">-Path</span></span>
<span data-ttu-id="85276-119">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="85276-120">-확인</span><span class="sxs-lookup"><span data-stu-id="85276-120">-Confirm</span></span>
<span data-ttu-id="85276-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85276-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85276-122">-WhatIf</span></span>
<span data-ttu-id="85276-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85276-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85276-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85276-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85276-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85276-125">-DefaultProfile</span></span>
<span data-ttu-id="85276-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85276-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85276-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85276-127">CommonParameters</span></span>
<span data-ttu-id="85276-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85276-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85276-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85276-130">입력</span><span class="sxs-lookup"><span data-stu-id="85276-130">INPUTS</span></span>

### <span data-ttu-id="85276-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="85276-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="85276-132">' Acl ' 매개 변수는 파이프라인에서 ' DataLakeStoreItemAce [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85276-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="85276-133">출력</span><span class="sxs-lookup"><span data-stu-id="85276-133">OUTPUTS</span></span>

### <span data-ttu-id="85276-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="85276-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="85276-135">PassThru를 지정 하면 ACL 엔트리의 결과 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85276-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="85276-136">상속자</span><span class="sxs-lookup"><span data-stu-id="85276-136">NOTES</span></span>

## <span data-ttu-id="85276-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85276-137">RELATED LINKS</span></span>

