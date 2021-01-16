---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376265"
---
# <span data-ttu-id="68f94-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="68f94-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="68f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68f94-102">SYNOPSIS</span></span>
<span data-ttu-id="68f94-103">Azure Storage 계정에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="68f94-104">구문</span><span class="sxs-lookup"><span data-stu-id="68f94-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f94-105">설명</span><span class="sxs-lookup"><span data-stu-id="68f94-105">DESCRIPTION</span></span>
<span data-ttu-id="68f94-106">**Get-AzStorageAccountKey** cmdlet은 Azure Storage 계정에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="68f94-107">예제</span><span class="sxs-lookup"><span data-stu-id="68f94-107">EXAMPLES</span></span>

### <span data-ttu-id="68f94-108">예제 1: Storage 계정에 대한 액세스 키 얻기</span><span class="sxs-lookup"><span data-stu-id="68f94-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="68f94-109">이 명령은 지정된 Azure Storage 계정에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="68f94-110">예제 2: Storage 계정에 대한 특정 액세스 키 얻기</span><span class="sxs-lookup"><span data-stu-id="68f94-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="68f94-111">예제 3: Storage 계정에 대한 액세스 키를 나열하고 Kerberos 키(Active Directory를 사용하도록 설정된 경우)를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="68f94-112">이 명령은 지정된 Azure Storage 계정에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="68f94-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68f94-113">PARAMETERS</span></span>

### <span data-ttu-id="68f94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f94-114">-DefaultProfile</span></span>
<span data-ttu-id="68f94-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68f94-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="68f94-116">-ListKerbKey</span></span>
<span data-ttu-id="68f94-117">지정된 저장소 계정에 대한 Kerberos 키(Active Directory를 사용하도록 설정된 경우)를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="68f94-118">Kerberos 키는 Azure AD DS(Azure Active Directory Domain Service) 또는 AD DS(Active Directory Domain Service)를 사용하여 Azure Files ID 기반 인증을 위해 저장소 계정당 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="68f94-119">저장소 계정을 나타내는 도메인 서비스에 등록된 ID의 암호로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="68f94-120">Kerberos 키는 저장소 계정에 대한 제어 또는 데이터 평면 읽기 또는 쓰기 작업을 수행할 액세스 권한을 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="68f94-121">-Name</span><span class="sxs-lookup"><span data-stu-id="68f94-121">-Name</span></span>
<span data-ttu-id="68f94-122">이 cmdlet이 키를 받을 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="68f94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f94-123">-ResourceGroupName</span></span>
<span data-ttu-id="68f94-124">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="68f94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f94-125">CommonParameters</span></span>
<span data-ttu-id="68f94-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68f94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f94-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68f94-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f94-128">입력</span><span class="sxs-lookup"><span data-stu-id="68f94-128">INPUTS</span></span>

### <span data-ttu-id="68f94-129">System.String</span><span class="sxs-lookup"><span data-stu-id="68f94-129">System.String</span></span>

## <span data-ttu-id="68f94-130">출력</span><span class="sxs-lookup"><span data-stu-id="68f94-130">OUTPUTS</span></span>

### <span data-ttu-id="68f94-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="68f94-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="68f94-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68f94-132">NOTES</span></span>

## <span data-ttu-id="68f94-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68f94-133">RELATED LINKS</span></span>

[<span data-ttu-id="68f94-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="68f94-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


