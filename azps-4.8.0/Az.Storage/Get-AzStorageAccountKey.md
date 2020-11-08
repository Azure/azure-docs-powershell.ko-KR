---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213815"
---
# <span data-ttu-id="92f64-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="92f64-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="92f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f64-102">SYNOPSIS</span></span>
<span data-ttu-id="92f64-103">Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="92f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92f64-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92f64-105">DESCRIPTION</span></span>
<span data-ttu-id="92f64-106">**AzStorageAccountKey** Cmdlet은 Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="92f64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="92f64-107">EXAMPLES</span></span>

### <span data-ttu-id="92f64-108">예제 1: 저장소 계정의 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="92f64-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="92f64-109">이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="92f64-110">예제 2: 저장소 계정에 대 한 특정 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="92f64-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="92f64-111">예제 3: 저장소 계정의 선택 키 목록, Kerberos 키 포함 (active directory를 사용 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="92f64-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="92f64-112">이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="92f64-113">변수</span><span class="sxs-lookup"><span data-stu-id="92f64-113">PARAMETERS</span></span>

### <span data-ttu-id="92f64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f64-114">-DefaultProfile</span></span>
<span data-ttu-id="92f64-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f64-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="92f64-116">-ListKerbKey</span></span>
<span data-ttu-id="92f64-117">지정 된 저장소 계정에 대 한 Kerberos 키 (active directory를 사용할 수 있는 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="92f64-118">Azure 파일 id 기반 인증에 대 한 저장소 계정 당 Kerberos 키가 생성 됩니다 (azure AD DS (active Directory 도메인 서비스) 또는 AD DS (Active Directory 도메인 서비스).</span><span class="sxs-lookup"><span data-stu-id="92f64-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="92f64-119">저장소 계정을 나타내는 도메인 서비스에 등록 된 id의 암호로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="92f64-120">Kerberos 키는 저장소 계정에 대 한 모든 컨트롤 또는 데이터 평면 읽기 또는 쓰기 작업을 수행할 수 있는 액세스 권한을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="92f64-121">-이름</span><span class="sxs-lookup"><span data-stu-id="92f64-121">-Name</span></span>
<span data-ttu-id="92f64-122">이 cmdlet에서 키를 가져오는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f64-123">-ResourceGroupName</span></span>
<span data-ttu-id="92f64-124">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-124">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f64-125">CommonParameters</span></span>
<span data-ttu-id="92f64-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f64-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f64-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f64-128">입력</span><span class="sxs-lookup"><span data-stu-id="92f64-128">INPUTS</span></span>

### <span data-ttu-id="92f64-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="92f64-129">System.String</span></span>

## <span data-ttu-id="92f64-130">출력</span><span class="sxs-lookup"><span data-stu-id="92f64-130">OUTPUTS</span></span>

### <span data-ttu-id="92f64-131">StorageAccountKey를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f64-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="92f64-132">상속자</span><span class="sxs-lookup"><span data-stu-id="92f64-132">NOTES</span></span>

## <span data-ttu-id="92f64-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92f64-133">RELATED LINKS</span></span>

[<span data-ttu-id="92f64-134">새로운 AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="92f64-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


