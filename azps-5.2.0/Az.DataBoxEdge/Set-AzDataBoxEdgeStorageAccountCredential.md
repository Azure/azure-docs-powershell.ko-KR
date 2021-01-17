---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360865"
---
# <span data-ttu-id="3d62c-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3d62c-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3d62c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d62c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d62c-103">디바이스에 대한 저장소 계정 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="3d62c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d62c-104">SYNTAX</span></span>

### <span data-ttu-id="3d62c-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d62c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d62c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d62c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d62c-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d62c-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d62c-108">설명</span><span class="sxs-lookup"><span data-stu-id="3d62c-108">DESCRIPTION</span></span>
<span data-ttu-id="3d62c-109">**Set-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스의 저장소 계정에 해당하는 저장소 계정 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="3d62c-110">예제</span><span class="sxs-lookup"><span data-stu-id="3d62c-110">EXAMPLES</span></span>

### <span data-ttu-id="3d62c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d62c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="3d62c-112">저장소 계정에 대한 액세스 키를 회전하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="3d62c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d62c-113">PARAMETERS</span></span>

### <span data-ttu-id="3d62c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d62c-114">-AsJob</span></span>
<span data-ttu-id="3d62c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d62c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d62c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d62c-116">-DefaultProfile</span></span>
<span data-ttu-id="3d62c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d62c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3d62c-118">-DeviceName</span></span>
<span data-ttu-id="3d62c-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="3d62c-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3d62c-120">-EncryptionKey</span></span>
<span data-ttu-id="3d62c-121">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="3d62c-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d62c-122">-InputObject</span></span>
<span data-ttu-id="3d62c-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="3d62c-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d62c-124">-Name</span></span>
<span data-ttu-id="3d62c-125">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="3d62c-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d62c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d62c-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3d62c-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d62c-128">-ResourceId</span></span>
<span data-ttu-id="3d62c-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d62c-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="3d62c-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="3d62c-131">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="3d62c-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d62c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d62c-132">-Confirm</span></span>
<span data-ttu-id="3d62c-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d62c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d62c-134">-WhatIf</span></span>
<span data-ttu-id="3d62c-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3d62c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d62c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d62c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d62c-137">CommonParameters</span></span>
<span data-ttu-id="3d62c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d62c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d62c-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d62c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d62c-140">입력</span><span class="sxs-lookup"><span data-stu-id="3d62c-140">INPUTS</span></span>

### <span data-ttu-id="3d62c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3d62c-141">System.String</span></span>

### <span data-ttu-id="3d62c-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3d62c-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3d62c-143">출력</span><span class="sxs-lookup"><span data-stu-id="3d62c-143">OUTPUTS</span></span>

### <span data-ttu-id="3d62c-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3d62c-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3d62c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d62c-145">NOTES</span></span>

## <span data-ttu-id="3d62c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d62c-146">RELATED LINKS</span></span>
