---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528817"
---
# <span data-ttu-id="81a22-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="81a22-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="81a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a22-102">SYNOPSIS</span></span>
<span data-ttu-id="81a22-103">노드에서 Windows PowerShell 스크립트 블록을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81a22-104">SYNTAX</span></span>

### <span data-ttu-id="81a22-105">ByName</span><span class="sxs-lookup"><span data-stu-id="81a22-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81a22-106">BySession</span><span class="sxs-lookup"><span data-stu-id="81a22-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a22-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81a22-107">DESCRIPTION</span></span>
<span data-ttu-id="81a22-108">**AzureRmServerManagementPowerShellCommand** Cmdlet은 Azure 서버 관리 게이트웨이에서 관리 되는 노드에서 Windows PowerShell 스크립트 블록을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="81a22-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81a22-109">EXAMPLES</span></span>

## <span data-ttu-id="81a22-110">변수</span><span class="sxs-lookup"><span data-stu-id="81a22-110">PARAMETERS</span></span>

### <span data-ttu-id="81a22-111">-명령</span><span class="sxs-lookup"><span data-stu-id="81a22-111">-Command</span></span>
<span data-ttu-id="81a22-112">대상 노드에서 실행할 스크립트 블록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a22-113">-DefaultProfile</span></span>
<span data-ttu-id="81a22-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="81a22-115">-NodeName</span></span>
<span data-ttu-id="81a22-116">스크립트 블록을 실행할 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-117">-PowerShellSessionName 이름</span><span class="sxs-lookup"><span data-stu-id="81a22-117">-PowerShellSessionName</span></span>
<span data-ttu-id="81a22-118">대상 노드의 Windows PowerShell 실행 공간 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="81a22-119">-RawOutput</span></span>
<span data-ttu-id="81a22-120">Cmdlet이 노드의 출력을 포함 하는 전체 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a22-121">-ResourceGroupName</span></span>
<span data-ttu-id="81a22-122">노드가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-123">-세션</span><span class="sxs-lookup"><span data-stu-id="81a22-123">-Session</span></span>
<span data-ttu-id="81a22-124">이 cmdlet이 대상 노드에 연결 하는 데 사용 하는 **세션** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="81a22-125">이 매개 변수는 *ResourceGroupName* , *NodeName* , *세션 이름* 및 *powershellsessionname 이름* 매개 변수 대신 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-126">-세션 이름</span><span class="sxs-lookup"><span data-stu-id="81a22-126">-SessionName</span></span>
<span data-ttu-id="81a22-127">노드를 관리할 세션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a22-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a22-128">CommonParameters</span></span>
<span data-ttu-id="81a22-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a22-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a22-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a22-131">입력</span><span class="sxs-lookup"><span data-stu-id="81a22-131">INPUTS</span></span>

### <span data-ttu-id="81a22-132">세션만</span><span class="sxs-lookup"><span data-stu-id="81a22-132">Session</span></span>
<span data-ttu-id="81a22-133">' Session ' 매개 변수는 파이프라인에서 ' Session ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a22-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="81a22-134">출력</span><span class="sxs-lookup"><span data-stu-id="81a22-134">OUTPUTS</span></span>

### <span data-ttu-id="81a22-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="81a22-135">System.Object</span></span>

## <span data-ttu-id="81a22-136">상속자</span><span class="sxs-lookup"><span data-stu-id="81a22-136">NOTES</span></span>

## <span data-ttu-id="81a22-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81a22-137">RELATED LINKS</span></span>

[<span data-ttu-id="81a22-138">Azure 서버 관리 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81a22-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


