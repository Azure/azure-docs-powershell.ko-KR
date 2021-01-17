---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331977"
---
# <span data-ttu-id="c244d-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c244d-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="c244d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c244d-102">SYNOPSIS</span></span>
<span data-ttu-id="c244d-103">웹앱에 탑재할 Azure Storage 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="c244d-104">이 매개 변수를 매개 변수(-AzureStoragePath)로 사용하여 Set-AzWebApp Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c244d-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c244d-105">구문</span><span class="sxs-lookup"><span data-stu-id="c244d-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c244d-106">설명</span><span class="sxs-lookup"><span data-stu-id="c244d-106">DESCRIPTION</span></span>
<span data-ttu-id="c244d-107">웹앱 내에서 탑재할 Azure Storage 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="c244d-108">예제</span><span class="sxs-lookup"><span data-stu-id="c244d-108">EXAMPLES</span></span>

### <span data-ttu-id="c244d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c244d-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="c244d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c244d-110">PARAMETERS</span></span>

### <span data-ttu-id="c244d-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="c244d-111">-AccessKey</span></span>
<span data-ttu-id="c244d-112">Azure Storage 계정에 대한 액세스 키</span><span class="sxs-lookup"><span data-stu-id="c244d-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="c244d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c244d-113">-AccountName</span></span>
<span data-ttu-id="c244d-114">Azure Storage 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-114">Azure Storage account name.</span></span>
<span data-ttu-id="c244d-115">예: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c244d-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="c244d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c244d-116">-DefaultProfile</span></span>
<span data-ttu-id="c244d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c244d-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="c244d-118">-MountPath</span></span>
<span data-ttu-id="c244d-119">ShareName에서 지정한 공유가 노출되는 컨테이너의 경로</span><span class="sxs-lookup"><span data-stu-id="c244d-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="c244d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c244d-120">-Name</span></span>
<span data-ttu-id="c244d-121">Azure Storage 속성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="c244d-122">웹앱 또는 슬롯 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="c244d-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c244d-123">-ShareName</span></span>
<span data-ttu-id="c244d-124">컨테이너에 탑재할 공유의 이름</span><span class="sxs-lookup"><span data-stu-id="c244d-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="c244d-125">-Type</span><span class="sxs-lookup"><span data-stu-id="c244d-125">-Type</span></span>
<span data-ttu-id="c244d-126">Azure Storage 계정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="c244d-127">Windows 컨테이너는 Azure Files만 지원</span><span class="sxs-lookup"><span data-stu-id="c244d-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="c244d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c244d-128">-Confirm</span></span>
<span data-ttu-id="c244d-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c244d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c244d-130">-WhatIf</span></span>
<span data-ttu-id="c244d-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c244d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c244d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c244d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c244d-133">CommonParameters</span></span>
<span data-ttu-id="c244d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c244d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c244d-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c244d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c244d-136">입력</span><span class="sxs-lookup"><span data-stu-id="c244d-136">INPUTS</span></span>

### <span data-ttu-id="c244d-137">없음</span><span class="sxs-lookup"><span data-stu-id="c244d-137">None</span></span>

## <span data-ttu-id="c244d-138">출력</span><span class="sxs-lookup"><span data-stu-id="c244d-138">OUTPUTS</span></span>

### <span data-ttu-id="c244d-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c244d-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="c244d-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c244d-140">NOTES</span></span>

## <span data-ttu-id="c244d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c244d-141">RELATED LINKS</span></span>
