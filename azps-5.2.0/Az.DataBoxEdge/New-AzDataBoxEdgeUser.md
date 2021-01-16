---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355065"
---
# <span data-ttu-id="b7274-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b7274-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b7274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7274-102">SYNOPSIS</span></span>
<span data-ttu-id="b7274-103">디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="b7274-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7274-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7274-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7274-105">DESCRIPTION</span></span>
<span data-ttu-id="b7274-106">**New-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="b7274-107">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b7274-108">예제</span><span class="sxs-lookup"><span data-stu-id="b7274-108">EXAMPLES</span></span>

### <span data-ttu-id="b7274-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7274-109">Example 1</span></span>
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

## <span data-ttu-id="b7274-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7274-110">PARAMETERS</span></span>

### <span data-ttu-id="b7274-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7274-111">-AsJob</span></span>
<span data-ttu-id="b7274-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b7274-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7274-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7274-113">-DefaultProfile</span></span>
<span data-ttu-id="b7274-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7274-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b7274-115">-DeviceName</span></span>
<span data-ttu-id="b7274-116">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="b7274-116">Device Name</span></span>

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

### <span data-ttu-id="b7274-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b7274-117">-EncryptionKey</span></span>
<span data-ttu-id="b7274-118">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="b7274-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b7274-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7274-119">-Name</span></span>
<span data-ttu-id="b7274-120">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="b7274-120">Username</span></span>

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

### <span data-ttu-id="b7274-121">-Password</span><span class="sxs-lookup"><span data-stu-id="b7274-121">-Password</span></span>
<span data-ttu-id="b7274-122">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="b7274-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="b7274-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7274-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7274-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b7274-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b7274-125">-Type</span><span class="sxs-lookup"><span data-stu-id="b7274-125">-Type</span></span>
<span data-ttu-id="b7274-126">UserType 선택</span><span class="sxs-lookup"><span data-stu-id="b7274-126">Select UserType</span></span>

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

### <span data-ttu-id="b7274-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7274-127">-Confirm</span></span>
<span data-ttu-id="b7274-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7274-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7274-129">-WhatIf</span></span>
<span data-ttu-id="b7274-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7274-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7274-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7274-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7274-132">CommonParameters</span></span>
<span data-ttu-id="b7274-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7274-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7274-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7274-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7274-135">입력</span><span class="sxs-lookup"><span data-stu-id="b7274-135">INPUTS</span></span>

### <span data-ttu-id="b7274-136">없음</span><span class="sxs-lookup"><span data-stu-id="b7274-136">None</span></span>

## <span data-ttu-id="b7274-137">출력</span><span class="sxs-lookup"><span data-stu-id="b7274-137">OUTPUTS</span></span>

### <span data-ttu-id="b7274-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b7274-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b7274-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7274-139">NOTES</span></span>

## <span data-ttu-id="b7274-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7274-140">RELATED LINKS</span></span>
