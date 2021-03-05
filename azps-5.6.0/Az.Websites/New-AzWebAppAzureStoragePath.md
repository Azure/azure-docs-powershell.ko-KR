---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: b30a7736c1d3971bcdd4d7b3b776b0c439e9395b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972352"
---
# <span data-ttu-id="724b9-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="724b9-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="724b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724b9-102">SYNOPSIS</span></span>
<span data-ttu-id="724b9-103">웹앱에 탑재할 Azure Storage 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="724b9-104">매개 변수(-AzureStoragePath)를 사용하여 Set-AzWebApp Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="724b9-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="724b9-105">구문</span><span class="sxs-lookup"><span data-stu-id="724b9-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="724b9-106">설명</span><span class="sxs-lookup"><span data-stu-id="724b9-106">DESCRIPTION</span></span>
<span data-ttu-id="724b9-107">웹앱에 탑재할 Azure Storage 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="724b9-108">예제</span><span class="sxs-lookup"><span data-stu-id="724b9-108">EXAMPLES</span></span>

### <span data-ttu-id="724b9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="724b9-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="724b9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="724b9-110">PARAMETERS</span></span>

### <span data-ttu-id="724b9-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="724b9-111">-AccessKey</span></span>
<span data-ttu-id="724b9-112">Azure Storage 계정에 대한 액세스 키</span><span class="sxs-lookup"><span data-stu-id="724b9-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="724b9-113">-AccountName</span></span>
<span data-ttu-id="724b9-114">Azure Storage 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-114">Azure Storage account name.</span></span>
<span data-ttu-id="724b9-115">예: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="724b9-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724b9-116">-DefaultProfile</span></span>
<span data-ttu-id="724b9-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="724b9-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="724b9-118">-MountPath</span></span>
<span data-ttu-id="724b9-119">ShareName에서 지정한 공유가 노출되는 컨테이너의 경로</span><span class="sxs-lookup"><span data-stu-id="724b9-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="724b9-120">-Name</span></span>
<span data-ttu-id="724b9-121">Azure Storage 속성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="724b9-122">웹앱 또는 슬롯 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="724b9-123">-ShareName</span></span>
<span data-ttu-id="724b9-124">컨테이너에 탑재할 공유의 이름</span><span class="sxs-lookup"><span data-stu-id="724b9-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-125">-Type</span><span class="sxs-lookup"><span data-stu-id="724b9-125">-Type</span></span>
<span data-ttu-id="724b9-126">Azure Storage 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="724b9-127">Windows 컨테이너는 Azure 파일만 지원</span><span class="sxs-lookup"><span data-stu-id="724b9-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="724b9-128">-Confirm</span></span>
<span data-ttu-id="724b9-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724b9-130">-WhatIf</span></span>
<span data-ttu-id="724b9-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="724b9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724b9-133">CommonParameters</span></span>
<span data-ttu-id="724b9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="724b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724b9-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="724b9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724b9-136">입력</span><span class="sxs-lookup"><span data-stu-id="724b9-136">INPUTS</span></span>

### <span data-ttu-id="724b9-137">없음</span><span class="sxs-lookup"><span data-stu-id="724b9-137">None</span></span>

## <span data-ttu-id="724b9-138">출력</span><span class="sxs-lookup"><span data-stu-id="724b9-138">OUTPUTS</span></span>

### <span data-ttu-id="724b9-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="724b9-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="724b9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="724b9-140">NOTES</span></span>

## <span data-ttu-id="724b9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="724b9-141">RELATED LINKS</span></span>
