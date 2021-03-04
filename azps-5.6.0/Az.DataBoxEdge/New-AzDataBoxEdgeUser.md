---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 6abc37d37bf06025389329b8b917db8a75cefd1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990313"
---
# <span data-ttu-id="d3a96-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="d3a96-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="d3a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a96-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a96-103">디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="d3a96-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3a96-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a96-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3a96-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a96-106">**New-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="d3a96-107">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="d3a96-108">예제</span><span class="sxs-lookup"><span data-stu-id="d3a96-108">EXAMPLES</span></span>

### <span data-ttu-id="d3a96-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3a96-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="d3a96-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3a96-110">PARAMETERS</span></span>

### <span data-ttu-id="d3a96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3a96-111">-AsJob</span></span>
<span data-ttu-id="d3a96-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3a96-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3a96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a96-113">-DefaultProfile</span></span>
<span data-ttu-id="d3a96-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a96-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3a96-115">-DeviceName</span></span>
<span data-ttu-id="d3a96-116">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="d3a96-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d3a96-117">-EncryptionKey</span></span>
<span data-ttu-id="d3a96-118">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="d3a96-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d3a96-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a96-119">-Name</span></span>
<span data-ttu-id="d3a96-120">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="d3a96-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-121">-Password</span><span class="sxs-lookup"><span data-stu-id="d3a96-121">-Password</span></span>
<span data-ttu-id="d3a96-122">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="d3a96-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="d3a96-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a96-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3a96-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d3a96-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-125">-Type</span><span class="sxs-lookup"><span data-stu-id="d3a96-125">-Type</span></span>
<span data-ttu-id="d3a96-126">UserType 선택</span><span class="sxs-lookup"><span data-stu-id="d3a96-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-127">-확인</span><span class="sxs-lookup"><span data-stu-id="d3a96-127">-Confirm</span></span>
<span data-ttu-id="d3a96-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a96-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a96-129">-WhatIf</span></span>
<span data-ttu-id="d3a96-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a96-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a96-132">CommonParameters</span></span>
<span data-ttu-id="d3a96-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a96-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a96-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a96-135">입력</span><span class="sxs-lookup"><span data-stu-id="d3a96-135">INPUTS</span></span>

### <span data-ttu-id="d3a96-136">없음</span><span class="sxs-lookup"><span data-stu-id="d3a96-136">None</span></span>

## <span data-ttu-id="d3a96-137">출력</span><span class="sxs-lookup"><span data-stu-id="d3a96-137">OUTPUTS</span></span>

### <span data-ttu-id="d3a96-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d3a96-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d3a96-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3a96-139">NOTES</span></span>

## <span data-ttu-id="d3a96-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3a96-140">RELATED LINKS</span></span>
