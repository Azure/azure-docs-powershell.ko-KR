---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 89901fc41cc3b05530d3f6980d82e28382dcd1a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875966"
---
# <span data-ttu-id="d4b80-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d4b80-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d4b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b80-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b80-103">장치에 대 한 저장소 계정 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="d4b80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4b80-104">SYNTAX</span></span>

### <span data-ttu-id="d4b80-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d4b80-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b80-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b80-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4b80-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b80-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b80-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d4b80-108">DESCRIPTION</span></span>
<span data-ttu-id="d4b80-109">**AzDataBoxEdgeStorageAccountCredential** Cmdlet은 데이터 상자에 지 장치의 저장소 계정에 해당 하는 저장소 계정 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="d4b80-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d4b80-110">EXAMPLES</span></span>

### <span data-ttu-id="d4b80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4b80-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="d4b80-112">저장소 계정의 선택 키 회전에 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="d4b80-113">변수</span><span class="sxs-lookup"><span data-stu-id="d4b80-113">PARAMETERS</span></span>

### <span data-ttu-id="d4b80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4b80-114">-AsJob</span></span>
<span data-ttu-id="d4b80-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d4b80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4b80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b80-116">-DefaultProfile</span></span>
<span data-ttu-id="d4b80-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b80-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="d4b80-118">-DeviceName</span></span>
<span data-ttu-id="d4b80-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="d4b80-119">Device Name</span></span>

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

### <span data-ttu-id="d4b80-120">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="d4b80-120">-EncryptionKey</span></span>
<span data-ttu-id="d4b80-121">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="d4b80-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d4b80-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4b80-122">-InputObject</span></span>
<span data-ttu-id="d4b80-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="d4b80-123">Input Object</span></span>

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

### <span data-ttu-id="d4b80-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d4b80-124">-Name</span></span>
<span data-ttu-id="d4b80-125">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d4b80-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="d4b80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b80-126">-ResourceGroupName</span></span>
<span data-ttu-id="d4b80-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d4b80-127">Resource Group Name</span></span>

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

### <span data-ttu-id="d4b80-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b80-128">-ResourceId</span></span>
<span data-ttu-id="d4b80-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b80-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="d4b80-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="d4b80-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="d4b80-131">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="d4b80-131">provide storage account access key</span></span>

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

### <span data-ttu-id="d4b80-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d4b80-132">-Confirm</span></span>
<span data-ttu-id="d4b80-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b80-134">-WhatIf</span></span>
<span data-ttu-id="d4b80-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4b80-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b80-137">CommonParameters</span></span>
<span data-ttu-id="d4b80-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b80-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4b80-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b80-140">입력</span><span class="sxs-lookup"><span data-stu-id="d4b80-140">INPUTS</span></span>

### <span data-ttu-id="d4b80-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4b80-141">System.String</span></span>

### <span data-ttu-id="d4b80-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d4b80-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d4b80-143">출력</span><span class="sxs-lookup"><span data-stu-id="d4b80-143">OUTPUTS</span></span>

### <span data-ttu-id="d4b80-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d4b80-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d4b80-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d4b80-145">NOTES</span></span>

## <span data-ttu-id="d4b80-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4b80-146">RELATED LINKS</span></span>
